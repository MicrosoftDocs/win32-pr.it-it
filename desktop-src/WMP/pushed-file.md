---
title: File di cui è stato push
description: File di cui è stato push
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, file di grafica
- skins, file art
- file per le interfaccia, grafica
- file di grafica per le interfaccia, file di cui è stato push
- Windows Media Player Interfaccia per dispositivi mobili, file di cui è stato push
- skins, push di file
- Push di file nelle interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0526cad560abfbee3a7ec6cbaa0c355a51d93c2080d7c1ef933f7caaf867ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570677"
---
# <a name="pushed-file"></a>File di cui è stato push

Il file push contiene le immagini che verranno visualizzate quando l'utente tocca un pulsante. È anche possibile includere le immagini normali e di cui è stato premuto il push per lo stato di sospensione del pulsante PlayPause.

L'immagine seguente è un tipico file di push.

![File di cui è stato push](images/cesdkpus.png)

In questo modo vengono archiviate le immagini che verranno visualizzate quando si toccano i pulsanti del tipo di clic. In questo file sono archiviate anche le immagini normali e di cui è stato premuto il push per l'immagine sospesa del pulsante PlayPause. Ad eccezione delle immagini secondarie PlayPause a destra, le altre immagini pulsante si allineano con l'immagine di sfondo, usando l'offset definito nella sezione Bitmaps del file di definizione dell'interfaccia.

Si noti che lo sfondo dell'immagine del pulsante corrisponde esattamente all'area corrispondente nel file Di sfondo. Questo è importante, perché quando l'utente tocca un pulsante di tipo hit type, l'intero rettangolo definito per l'immagine inserita sostituirà l'area corrispondente nel file di sfondo. Mantenere l'immagine coerente con l'immagine di sfondo per assicurarsi che cambino effettivamente solo le parti del pulsante che si vuole visualizzare in modo diverso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di grafica**](art-files-mobile.md)
</dt> </dl>

 

 




