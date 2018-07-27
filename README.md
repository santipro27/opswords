using Terraria.ID;
using Terraria.ModLoader;

namespace prueba.Items
{
	public class minigun : ModItem
	{
		public override void SetStaticDefaults()
		{
			DisplayName.SetDefault("minigun");
			Tooltip.SetDefault("una pistola pequeña.");
		}
		public override void SetDefaults()
		{
        item.damage = 30;
        item.ranged = true;
        item.width =8; //Tamaño de Ancho
        item.height = 2; //Tamaño de Alto
        item.useTime = 30; //mientras mas alto sea el useTime mas lenta será el arma. Usa un bajo UseTime para que el arma sea Rapida
        item.useAnimation = 20;
        item.useStyle = 5; //Dejar en 5 para que el personaje use el arma de forma normal
        item.noMelee = true;
        item.knockBack = 5;
        item.value = 1000000; //Precio
        item.rare = 3;
		item.UseSound = SoundID.Item38;
        item.autoReuse = false;
        item.shoot = 10; //dejar en 10 para que dispare balas normales
        item.shootSpeed = 2f;
        item.useAmmo = AmmoID.Bullet;
		}

		public override void AddRecipes()
		{
			ModRecipe recipe = new ModRecipe(mod);
			recipe.AddIngredient(ItemID.FlintlockPistol, 2);
			recipe.AddTile(TileID.WorkBenches);
			recipe.SetResult(this);
			recipe.AddRecipe();
		}
	}
}
