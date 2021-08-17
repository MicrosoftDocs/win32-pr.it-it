---
title: Elementi obbligatori
description: Elementi obbligatori
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, elementi
- skins,elements
- file di definizione dell'interfaccia utente,elementi
- elementi, file di definizione dell'interfaccia
- elementi, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18433e20c914cdc4b276857f97aab6a692d1d11c811660c73620b09a5b9a0f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746310"
---
# <a name="required-elements"></a>Elementi obbligatori

È necessario specificare gli elementi seguenti nel file di definizione dell'interfaccia:

-   **Intestazione.** L'intestazione del file di definizione dell'interfaccia principale è obbligatoria. Per informazioni sulla versione dell'intestazione, vedere la tabella nella [sezione Creazione di un file di definizione dell'interfaccia](creating-a-skin-definition-file.md) utente.
-   **Sezione Descrizione.** La sezione Descrizione è obbligatoria quando si creano le interfaccia per Windows Media Player serie 9 per Windows Mobile. Deve essere la prima sezione del file di definizione dell'interfaccia e deve specificare valori validi per Dimensions. Specificare un valore per Orientation è facoltativo.
-   **Sezione Bitmap.** La sezione Bitmaps è obbligatoria. Inoltre, la sezione Bitmaps deve specificare nomi validi per i file di immagine Background, Disabled, Pushed, Region e Super.
-   **file di immagine.** È necessario specificare i file di immagine Background, Disabled, Pushed, Region e Super come parte dell'interfaccia. Se si creano le interfaccia per Windows Media Player 10 Mobile o versione successiva, non è necessario includere file di immagine Region o Super.

Se si crea un'interfaccia con solo immagini definite, l'interfaccia sarà visibile, ma non offrirà alcuna funzionalità significativa all'utente. Se si decide di creare un'interfaccia senza pulsanti, ad esempio per impedire all'utente di ignorare determinati contenuti, tenere presente che potrebbe essere comunque possibile eseguire il mapping delle funzionalità ai pulsanti hardware nel dispositivo.

I file thumb sono necessari e i trackbar non possono essere usati senza il cursore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di definizione dell'interfaccia**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




