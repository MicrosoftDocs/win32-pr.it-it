---
title: File di area
description: File di area
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di immagine per le interfacce, i file di area
- Interfacce di Windows Media Player Mobile, file di area
- interfacce, file di area
- File di area in interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332111"
---
# <a name="region-files"></a>File di area

I file di area sono necessari se si usa qualsiasi tipo di pulsante di hit (2PushHit, PushHit o ToggleHit).

I file di area vengono usati per definire aree che risponderanno a un tocco, noto anche come hit, su un pulsante specifico. Per ogni pulsante hit, a un'area nella bitmap dell'area viene assegnato un colore Web specifico, ad esempio \# FF0000, che rappresenta il valore di rosso a tinta unita. Il numero di colore viene specificato nella definizione del pulsante Region. Quando l'utente Visualizza l'interfaccia, l'immagine del pulsante viene sovrapposta allo sfondo usando le coordinate dell'area nella bitmap della regione.

Ad esempio, è possibile creare un cerchio rosso in una posizione corrispondente alla posizione del pulsante Avanti e colorarlo a tinta unita rossa ( \# FF0000). Nella definizione del pulsante è quindi possibile assegnare un valore RGB raggiunto di 255, 0, 0, ovvero l'equivalente RGB di \# ff0000. In questo caso, il pulsante Avanti risponderà solo ai tocchi (riscontri) all'interno del cerchio rosso.

I pulsanti hit vengono usati quando si desidera definire forme diverse dai rettangoli. È comunque necessario definire le coordinate per ciascun pulsante in modo che le immagini secondarie come push e Disable possano trovarsi correttamente. In pratica, ogni pulsante è limitato da un rettangolo e questi rettangoli di limite immaginari non devono sovrapporsi.

> [!Note]  
> I file di arte dell'area non sono necessari nelle interfacce Windows Media Player 10 mobile perché i tipi di pulsante non sono supportati in Windows Media Player 10 mobile o versioni successive.

 

L'immagine seguente è un file di area tipico.

![file Region](images/cesdkreg.png)

Questo file definisce le parti dell'interfaccia per ogni pulsante di tipo hit. Ogni colore verrà identificato in base al relativo numero di colore nella sezione dei pulsanti del file di definizione dell'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di immagine**](art-files-mobile.md)
</dt> </dl>

 

 




