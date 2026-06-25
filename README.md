export interface Recipe {
  id: string;
  name: string;
  country: string;
  continent: string;
  image: string;
  prepTime: number;
  cookTime: number;
  servings: number;
  difficulty: 'facile' | 'moyen' | 'difficile';
  category: 'entree' | 'soupe' | 'salade' | 'plat-principal' | 'dessert' | 'viennoiserie' | 'boisson' | 'street-food';
  tags: string[];
  ingredients: Ingredient[];
  steps: string[];
  tips: string[];
  nutrition: NutritionInfo;
  history: string;
  presentation: string;
  similar: string[];
  rating: number;
  reviews: number;
  description: string;
}

export interface Ingredient {
  name: string;
  amount: string;
  unit: string;
}

export interface NutritionInfo {
  calories: number;
  protein: number;
  carbs: number;
  fat: number;
  fiber: number;
}

export interface FilterOptions {
  countries: string[];
  continents: string[];
  categories: string[];
  difficulty: string[];
  maxPrepTime: number;
  tags: string[];
  searchQuery: string;
}

export interface User {
  favorites: string[];
  ratings: Record<string, number>;
  theme: 'light' | 'dark';
  language: 'fr' | 'en' | 'es';
}
