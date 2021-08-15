---
description: Descrive un disco rigido, il partizionamento e il record di avvio master.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Dispositivi disco e partizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758454c9fc9e684e918646bf99869c7544b3b02c0201eb2ba507f8ffbdc303d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015375"
---
# <a name="disk-devices-and-partitions"></a>Dispositivi disco e partizioni

Un disco rigido è costituito da un set di dischi in pila, ognuno dei quali contiene dati archiviati in modo integro in cerchi concentrici o *tracce*. Ogni vassoio ha due teste, una su ogni lato del disco, che legge o scrive i dati mentre il disco ruota. *Un'unità disco rigido* controlla il posizionamento, la lettura e la scrittura del disco rigido. Si noti che le teste di tutti i vassoi sono posizionate come unità.

L'unità indirizzabile più piccola di una traccia è un *settore*. Un *cilindro* è definito come il set di tracce che appaiono nella stessa posizione su ogni piatto. Ad esempio, il diagramma seguente mostra un disco rigido con quattro dischi. Il cilindro X è costituito da otto tracce (traccia X da ogni lato di ogni tracciato).

![disco rigido, inclusi tracce, settori e dischi](images/diskdevice.png)

Un disco rigido può contenere una o più aree logiche denominate *partizioni*. Le partizioni vengono create quando l'utente formatta un disco rigido come *disco di base.* Windows supporta anche *dischi dinamici*, che non sono descritti in questo argomento. Per altre informazioni sui dischi di base e dinamici, vedere [Dischi di base e dinamici.](basic-and-dynamic-disks.md)

La creazione di più partizioni su un disco consente di avere dischi rigidi separati. Ad esempio, un sistema con un disco rigido con una partizione contiene un singolo volume, designato dal sistema come unità C. Un sistema con un disco rigido con due partizioni contiene in genere unità C e D. La presenza di più partizioni su un disco rigido può semplificare la gestione del sistema, ad esempio l'organizzazione dei file o il supporto di più utenti.

Il primo settore fisico in un disco di base contiene una struttura di dati nota come MBR (Master Boot Record). L'MBR contiene quanto segue:

-   Un programma di avvio (fino a 442 byte)
-   Firma del disco (numero univoco a 4 byte)
-   Una tabella di partizione (fino a quattro voci)
-   Marcatore di fine MBR (sempre 0x55AA)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla gestione dei volumi](about-volume-management.md)
</dt> <dt>

[Dischi di base e dinamici](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



