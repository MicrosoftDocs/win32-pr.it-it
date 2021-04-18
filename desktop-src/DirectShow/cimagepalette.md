---
description: La classe CImagePalette gestisce le tavolozze per i renderer video. Può essere usato per creare una tavolozza logica da un formato video. Questa classe è destinata all'uso con le classi CBaseWindow e CDrawImage, quindi è in qualche modo specializzata.
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
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303786"
---
# <a name="cimagepalette-class"></a>Classe CImagePalette

La `CImagePalette` classe gestisce le tavolozze per i renderer video. Può essere usato per creare una tavolozza logica da un formato video. Questa classe è destinata all'uso con le classi [**CBaseWindow**](cbasewindow.md) e [**CDrawImage**](cdrawimage.md) , quindi è in qualche modo specializzata.



| Variabili membro protette                                       | Descrizione                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**\_hPalette m**](cimagepalette-m-hpalette.md)                  | Handle per la tavolozza logica gestita da questo oggetto.                                        |
| [**\_pBaseWindow m**](cimagepalette-m-pbasewindow.md)            | Puntatore all'oggetto **CBaseWindow** che gestisce la finestra.                                 |
| [**\_pDrawImage m**](cimagepalette-m-pdrawimage.md)              | Puntatore all'oggetto **CDrawImage** che disegna l'immagine del video.                               |
| [**\_pFilter m**](cimagepalette-m-pfilter.md)                    | Puntatore al filtro proprietario.                                                                  |
| Metodi pubblici                                                   | Descrizione                                                                                    |
| [**CImagePalette**](cimagepalette-cimagepalette.md)             | Metodo del costruttore.                                                                            |
| [**CopyPalette**](cimagepalette-copypalette.md)                 | Copia la tavolozza da qualsiasi struttura **VIDEOINFO** a qualsiasi struttura **VIDEOINFO** di pallettizzati. |
| [**MakeIdentityPalette**](cimagepalette-makeidentitypalette.md) | Tenta di creare una tavolozza che esegue il mapping direttamente alla tavolozza selezionata nel dispositivo di visualizzazione.   |
| [**MakePalette**](cimagepalette-makepalette.md)                 | Crea una tavolozza logica dalla tabella dei colori in un formato video.                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | Imposta una tavolozza in base a un tipo di supporto dal filtro proprietario.                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | Elimina la tavolozza logica esistente.                                                          |



 

 

 



