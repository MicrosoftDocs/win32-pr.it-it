---
title: File con privilegi avanzati
description: File con privilegi avanzati
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, file con file con privilegi avanzati
- Windows Media Player Mobile Skins, file con file con privilegi avanzati
- interfacce, file con privilegi avanzati
- File con privilegi avanzati nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298743"
---
# <a name="super-files"></a>File con privilegi avanzati

I file con privilegi avanzati vengono usati per archiviare le immagini disabilitate per trackbars. Poiché l'immagine TrackBar principale viene visualizzata nel file in background e l'utente tocca l'immagine Thumb, non l'immagine TrackBar, per trackbars è necessaria solo l'immagine disabilitata. Viene archiviato nel file definito da Super nella sezione bitmap del file di definizione dell'interfaccia personalizzata. Un file con privilegi avanzati può archiviare anche le immagini inserite e disabilitate per altri pulsanti, ad esempio mute, che non devono necessariamente essere un pulsante di tipo hit.

> [!Note]  
> I file Super Art non vengono usati nelle interfacce per Windows Media Player 10 mobile o versioni successive perché le immagini disabilitate per Seek trackbars si trovano nel file seekthumb.

 

L'immagine seguente è un file Super tipico.

![file con privilegi avanzati](images/cesdksup.png)

Consente di archiviare le immagini disabilitate per i TrackBar e il pulsante di disattivazione. Queste immagini sono offset in base a quanto definito dalla sezione bitmap.

L'area di sfondo dell'immagine TrackBar disabilitata corrisponde esattamente all'area corrispondente nel file in background. Questo è importante, poiché l'intero rettangolo definito per l'immagine TrackBar disabilitata sostituirà l'area corrispondente nel file in background. Ciò garantisce che l'immagine TrackBar disabilitata si mescoli facilmente nell'immagine di sfondo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di immagine**](art-files-mobile.md)
</dt> </dl>

 

 




