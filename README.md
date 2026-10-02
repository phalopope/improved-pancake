# improved-pancake
from fastapi import FastAPI from pydantic import BaseModel  app = FastAPI()  class Film(BaseModel):     titre: str     personnages: list[str]     histoire: str  @app.post("/generer") def generer(film: Film):     scenes = [         f"{film.personnages[0]} rencontre {film.personnages[1]}",         film.histoire,         f"{film.personnage
