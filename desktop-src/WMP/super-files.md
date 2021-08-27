---
title: Super Files
description: Super Files
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, file di grafica
- skins, file art
- file per le interfaccia, grafica
- file di grafica per le interfaccia, file con privilegi di super
- Windows Media Player Interfaccia per dispositivi mobili, file con privilegi di super
- skins, super files
- Super files in skins (File con privilegi super nelle interfaccia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbd6734e0491b5fc0e6552db14b3c0ab4489e466e7851ef4b474e84d2d85183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122866"
---
# <a name="super-files"></a>Super Files

I file con privilegi più grandi vengono usati per archiviare le immagini disabilitate per i trackbar. Poiché l'immagine principale del trackbar viene visualizzata nel file di sfondo e l'utente tocca l'immagine thumb, non l'immagine del trackbar, per i trackbar è necessaria solo l'immagine Disabled. Viene archiviato nel file definito da Super nella sezione Bitmaps del file di definizione dell'interfaccia. Un file Super può anche archiviare le immagini Push e Disabled per altri pulsanti, ad esempio Disattiva, che non devono essere un pulsante di tipo clic.

> [!Note]  
> I file super art non vengono usati nelle interfaccia per Windows Media Player 10 Mobile o versioni successive perché le immagini disabilitate per i trackbar di ricerca si trovano nel file seekthumb.

 

L'immagine seguente è un tipico file Super.

![super file](images/cesdksup.png)

In questo modo vengono archiviate le immagini disabilitate per i trackbar e il pulsante disattiva audio. Queste immagini vengono offset come definito dalla sezione Bitmap.

L'area di sfondo dell'immagine del trackbar disabilitata corrisponde esattamente all'area corrispondente nel file Di sfondo. Questo è importante perché l'intero rettangolo definito per l'immagine del trackbar disabilitato sostituirà l'area corrispondente nel file di sfondo. Ciò garantisce che l'immagine del trackbar disabilitata si sfusi senza problemi nell'immagine di sfondo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di grafica**](art-files-mobile.md)
</dt> </dl>

 

 




