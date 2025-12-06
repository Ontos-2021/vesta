---
trigger: model_decision
---

{
  "brand": "Vesta",
  "currency": "ARS",
  "global_notes": {
    "description": "Óleos y sérums botánicos elaborados con procesos lentos de decocción, maceración, estacionamiento y decantación. Ingredientes de procedencia orgánica y/o agroecológica.",
    "potions_usage": "Todas las pociones son aptas para uso facial, capilar y corporal.",
    "serum_rose_usage": "El Serum Nocturno Rose es solo facial, no se recomienda para uso capilar."
  },
  "price_tables": {
    "pociones": [
      { "size_ml": 30, "price_ars": 33000 },
      { "size_ml": 50, "price_ars": 45000 },
      { "size_ml": 125, "price_ars": 100000 }
    ],
    "serum_nocturno_rose": [
      { "size_ml": 30, "price_ars": 33000 },
      { "size_ml": 50, "price_ars": 60000 }
    ]
  },
  "categories": [
    {
      "slug": "pociones-oleos",
      "name": "Pociones · Óleos multiuso",
      "short_description": "Óleos botánicos multiuso para rostro, cuerpo y cabello.",
      "products": [
        {
          "slug": "pocion-amor",
          "name": "Poción Amor",
          "type": "oleo_multiuso",
          "tags": ["facial", "corporal", "capilar", "emocional", "antiestres"],
          "aromas_principales": ["ylang ylang", "vainilla", "mandarina"],
          "ingredientes_base": [
            "óleo de semilla de damasco",
            "óleo de sésamo",
            "componentes antioxidantes y rejuvenecedores"
          ],
          "short_description": "Óleo nutritivo y revitalizante para piel y cabello, pensado para acompañar procesos de autocuidado y autoconfianza.",
          "beneficios_cosmeticos": [
            "nutre la piel",
            "hidrata en profundidad",
            "aporta frescura y sensación de limpieza",
            "revitaliza el aspecto general de la piel"
          ],
          "beneficios_energeticos_emocionales": [
            "ayuda a disipar miedos",
            "favorece pensamientos positivos",
            "fomenta la autoconfianza",
            "relaja el sistema nervioso",
            "promueve una sensación general de bienestar",
            "ideal para momentos de gran desgaste"
          ],
          "uso_recomendado": "Aplicar unas gotas sobre piel limpia o sobre el cabello, masajeando suavemente hasta su absorción. Puede utilizarse en rostro, cuerpo y puntas capilares.",
          "available_sizes_ml": [30, 50, 125],
          "price_table_reference": "pociones"
        },
        {
          "slug": "pocion-lumina",
          "name": "Poción Lumina",
          "type": "oleo_multiuso",
          "tags": ["facial", "corporal", "capilar", "calmante", "piel-irritada"],
          "aromas_principales": ["vainilla"],
          "ingredientes_base": [
            "maceración de caléndula",
            "apoyo botánico de vainilla"
          ],
          "short_description": "Óleo calmante y luminoso a base de caléndula y vainilla, ideal para pieles sensibles o irritadas.",
          "beneficios_cosmeticos": [
            "calma la piel",
            "posee acción antiinflamatoria",
            "favorece la cicatrización",
            "ideal para pieles irritadas o enrojecidas"
          ],
          "beneficios_energeticos_emocionales": [
            "aporta sensación de luz y resplandor",
            "ayuda a expresar la verdadera esencia de cada persona",
            "acompaña procesos de autoexpresión y apertura"
          ],
          "uso_recomendado": "Aplicar unas gotas sobre las zonas a tratar y masajear hasta su absorción. Puede utilizarse en rostro, cuerpo y cuero cabelludo según necesidad.",
          "available_sizes_ml": [30, 50, 125],
          "price_table_reference": "pociones"
        },
        {
          "slug": "pocion-4",
          "name": "Poción N°4",
          "type": "oleo_multiuso",
          "tags": ["facial", "corporal", "capilar", "purificante", "rituales"],
          "aromas_principales": ["eucalipto", "alcanfor", "menta", "citronella"],
          "ingredientes_base": [
            "maceración de eucalipto",
            "apoyo botánico de alcanfor",
            "apoyo botánico de menta",
            "apoyo botánico de citronella"
          ],
          "short_description": "Óleo purificante y revitalizante con eucalipto, ideal para limpiar energía y acompañar inicios y cierres de ciclo.",
          "beneficios_cosmeticos": [
            "purifica la piel",
            "revitaliza la apariencia general",
            "aporta sensación de frescura"
          ],
          "beneficios_energeticos_emocionales": [
            "actúa como transmutador de energía",
            "favorece la conexión con la naturaleza interior",
            "ideal para rituales de inicio y cierre de ciclos"
          ],
          "uso_recomendado": "Aplicar en masaje sobre pecho, cuello, espalda o zonas de tensión. También puede utilizarse en cuero cabelludo y cuerpo según la sensibilidad de cada piel.",
          "available_sizes_ml": [30, 50, 125],
          "price_table_reference": "pociones"
        },
        {
          "slug": "pocion-6",
          "name": "Poción N°6",
          "type": "oleo_multiuso",
          "tags": ["facial", "corporal", "capilar", "regenerador", "control-oleosidad"],
          "aromas_principales": [
            "lavanda",
            "geranio",
            "eucalipto",
            "menta",
            "citronella",
            "alcanfor"
          ],
          "ingredientes_base": [
            "maceración de lavanda",
            "maceración de eucalipto",
            "apoyo botánico de geranio",
            "apoyo botánico de menta",
            "apoyo botánico de citronella",
            "apoyo botánico de alcanfor"
          ],
          "short_description": "Óleo regenerador y fortalecedor que limpia en profundidad piel y cuero cabelludo, ayudando a equilibrar la oleosidad.",
          "beneficios_cosmeticos": [
            "regenerador de la piel",
            "controla la oleosidad",
            "fortalece piel y cuero cabelludo",
            "limpieza profunda de piel y cuero cabelludo"
          ],
          "beneficios_energeticos_emocionales": [
            "acompaña procesos de renovación personal",
            "favorece la sensación de fortaleza interna"
          ],
          "uso_recomendado": "Aplicar en cuero cabelludo o zonas con tendencia oleosa, masajear y dejar actuar. También puede utilizarse en rostro y cuerpo según la tolerancia de la piel.",
          "available_sizes_ml": [30, 50, 125],
          "price_table_reference": "pociones"
        }
      ]
    },
    {
      "slug": "serums-faciales",
      "name": "Serums faciales",
      "short_description": "Fórmulas concentradas para cuidado intensivo de la piel del rostro.",
      "products": [
        {
          "slug": "serum-nocturno-rose",
          "name": "Serum Nocturno Rose",
          "type": "serum_facial_nocturno",
          "tags": ["facial", "nocturno", "antiage", "regenerador", "manchas"],
          "uso_capilar_permitido": false,
          "ingredientes_principales": [
            "aceite de rosa mosqueta",
            "vitamina A",
            "vitamina C",
            "vitamina E",
            "colágeno vegetal",
            "apoyo botánico de rosa"
          ],
          "short_description": "Sérum nocturno regenerador con rosa mosqueta, vitaminas y colágeno vegetal, pensado para hidratar, unificar el tono y acompañar procesos de reparación de la piel.",
          "beneficios_rosa_mosqueta": [
            "ayuda en la regeneración cutánea",
            "acción anti-age",
            "hidratación profunda",
            "contribuye a la reducción de manchas",
            "apoyo como tratamiento preventivo para estrías",
            "propiedades antiinflamatorias"
          ],
          "funciones_activos": {
            "vitamina_c": "Actúa como antioxidante, favorece la síntesis de colágeno y el material intercelular, con efecto anti-age.",
            "vitamina_e": "Antioxidante que protege el tejido corporal del daño causado por radicales libres y protege el colágeno.",
            "vitamina_a": "Relacionada con el metabolismo de la epidermis, ayuda a regular la queratina y estimula la regeneración desde la capa basal.",
            "colageno_vegetal": "Activo de origen vegetal que suaviza, protege, brinda firmeza y elasticidad a la piel."
          },
          "uso_recomendado": "Aplicar por la noche sobre piel limpia, antes o en lugar de la crema hidratante. Utilizar pocas gotas y masajear suavemente rostro y cuello evitando el contorno inmediato de los ojos.",
          "available_sizes_ml": [30, 50],
          "price_table_reference": "serum_nocturno_rose"
        }
      ]
    }
  ]
}
