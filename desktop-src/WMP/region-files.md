---
title: File di area
description: File di area
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Windows Media Player Skin per dispositivi mobili, file di grafica
- skins, file di grafica
- file per skin, art
- file di grafica per le skin, file di area
- Windows Media Player Skin per dispositivi mobili, file di area
- skins,File di area
- File di area nelle skin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ce26db27ef6ad3373916337c6378886a2846f71f1d8aa0e8d5266aae23eff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934091"
---
# <a name="region-files"></a>File di area

I file di area sono necessari se si usa qualsiasi tipo di pulsante di scelta (2PushHit, PushHit o ToggleHit).

I file di area vengono usati per definire le aree che risponderanno a un tocco, noto anche come clic, su un pulsante specifico. Per ogni pulsante di scelta, a un'area nella bitmap Region viene assegnato un colore Web specifico, ad esempio FF0000, che è il valore del \# rosso tinta unita. Il numero di colore viene specificato nella definizione del pulsante dell'area. Quando l'utente visualizza l'interfaccia utente, l'immagine del pulsante viene sovrapposta sullo sfondo usando le coordinate dell'area nella bitmap Region.

Ad esempio, è possibile disegnare un cerchio rosso in una posizione corrispondente alla posizione del pulsante Avanti e colorarlo di rosso a tinta unita ( \# FF0000). Nella definizione del pulsante è quindi possibile assegnare un valore RGB raggiunto pari a 255,0,0 (equivalente RGB \# di FF0000). In questo caso, il pulsante Avanti risponde solo ai tocchi (riscontri) all'interno del cerchio rosso.

I pulsanti di scelta vengono usati quando si vogliono definire forme diverse dai rettangoli. È comunque necessario definire le coordinate per ogni pulsante in modo che le immagini secondarie, ad esempio Push e Disabilitato, possano essere posizionate correttamente. In pratica, ogni pulsante è delimitato da un rettangolo e questi rettangoli limite immaginari non devono sovrapporsi.

> [!Note]  
> I file di immagine dell'area non sono necessari in Windows Media Player 10 skin per dispositivi mobili perché i tipi di pulsante non sono supportati in Windows Media Player 10 Mobile o versioni successive.

 

L'immagine seguente è un tipico file Region.

![file di area](images/cesdkreg.png)

Questo file definisce le parti dell'interfaccia per ogni pulsante di tipo hit. Ogni colore verrà identificato dal relativo numero di colore nella sezione Pulsanti del file di definizione dell'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di grafica**](art-files-mobile.md)
</dt> </dl>

 

 




