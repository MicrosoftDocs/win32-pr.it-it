---
description: La classe CImagePalette gestisce le tavolozze per i renderer video. Può essere usato per creare una tavolozza logica da un formato video. Questa classe deve essere usata con le classi CBaseWindow e CDrawImage, quindi è piuttosto specializzata.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Classe CImagePalette
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 390bd4fc60e7d20264ae3a9238699108e7778524b73c6af22038197260da4463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074065"
---
# <a name="cimagepalette-class"></a>Classe CImagePalette

La `CImagePalette` classe gestisce le tavolozze per i renderer video. Può essere usato per creare una tavolozza logica da un formato video. Questa classe deve essere usata con le classi [**CBaseWindow**](cbasewindow.md) e [**CDrawImage,**](cdrawimage.md) quindi è piuttosto specializzata.



| Variabili membro protette                                       | Descrizione                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ hPalette**](cimagepalette-m-hpalette.md)                  | Handle per il riquadro logico gestito da questo oggetto.                                        |
| [**m \_ pBaseWindow**](cimagepalette-m-pbasewindow.md)            | Puntatore **all'oggetto CBaseWindow** che gestisce la finestra.                                 |
| [**m \_ pDrawImage**](cimagepalette-m-pdrawimage.md)              | Puntatore **all'oggetto CDrawImage** che disegna l'immagine video.                               |
| [**m \_ pFilter**](cimagepalette-m-pfilter.md)                    | Puntatore al filtro proprietario.                                                                  |
| Metodi pubblici                                                   | Descrizione                                                                                    |
| [**CImagePalette**](cimagepalette-cimagepalette.md)             | Metodo del costruttore.                                                                            |
| [**CopiaPalette**](cimagepalette-copypalette.md)                 | Copia la tavolozza da qualsiasi **struttura VIDEOINFO** a qualsiasi struttura VIDEOINFO in **chiaro.** |
| [**MakeIdentityPalette**](cimagepalette-makeidentitypalette.md) | Tenta di creare una tavolozza mappata direttamente alla tavolozza selezionata nel dispositivo di visualizzazione.   |
| [**MakePalette**](cimagepalette-makepalette.md)                 | Crea una tavolozza logica dalla tabella dei colori in un formato video.                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | Configura un riquadro, in base a un tipo di supporto del filtro proprietario.                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | Elimina il riquadro logico esistente.                                                          |



 

 

 



