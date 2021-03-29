---
description: Classificazioni bitmap
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Classificazioni bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226714"
---
# <a name="bitmap-classifications"></a>Classificazioni bitmap

Esistono due classi di bitmap:

-   [Bitmap indipendenti dal dispositivo](device-independent-bitmaps.md) (DIB). Il formato del file DIB è stato progettato per garantire che le immagini bitmap create usando un'applicazione possano essere caricate e visualizzate in un'altra applicazione, mantenendo lo stesso aspetto dell'originale.

-   Le [bitmap dipendenti dal dispositivo](device-dependent-bitmaps.md) (DDB), note anche come bitmap GDI, erano le uniche bitmap disponibili nelle prime versioni di Microsoft Windows a 16 bit (prima della versione 3,0). Tuttavia, con il miglioramento della tecnologia di visualizzazione e con l'aumentare della varietà di dispositivi di visualizzazione disponibili, si verificano alcuni problemi intrinseci che possono essere risolti solo con la funzionalità DIB. Ad esempio, non esisteva alcun metodo di archiviazione (o recupero) della risoluzione del tipo di visualizzazione in cui è stata creata una bitmap, pertanto un'applicazione di disegno non è stata in grado di determinare rapidamente se una bitmap fosse adatta per il tipo di dispositivo di visualizzazione video in cui l'applicazione era in esecuzione.

    Nonostante questi problemi, DDB (noti anche come bitmap compatibili) sono ancora utili per migliorare le prestazioni GDI e per altre situazioni.

 

 



