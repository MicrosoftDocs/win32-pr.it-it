---
description: Descrive un disco rigido, il partizionamento e il record di avvio principale.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Dispositivi e partizioni disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568377"
---
# <a name="disk-devices-and-partitions"></a>Dispositivi e partizioni disco

Un disco rigido è costituito da un set di dischi in pila, ciascuno dei quali contiene dati archiviati in modo elettromagnetico nei cerchi concentrici o in *tracce*. Ogni piatto ha due teste, una su ogni lato del piatto, che legge o scrive dati come spine del disco. Un' *unità disco rigido* controlla il posizionamento, la lettura e la scrittura del disco rigido. Si noti che le intestazioni di tutti i dischi sono posizionate come unità.

La più piccola unità indirizzabile di una traccia è un *settore*. Un *cilindro* viene definito come il set di tracce visualizzate nella stessa posizione in ogni piatto. Il diagramma seguente, ad esempio, Mostra un disco rigido con quattro dischi. Il cilindro X è costituito da otto tracce (Track X da ogni lato di ogni piatto).

![disco rigido, inclusi tracce, settori e dischi](images/diskdevice.png)

Un disco rigido può contenere una o più aree logiche denominate *partizioni*. Le partizioni vengono create quando l'utente formatta un disco rigido come *disco di base*. Windows supporta inoltre i *dischi dinamici*, che non vengono discussi in questo argomento. Per altre informazioni sui dischi di base e i dischi dinamici, vedere [dischi di base e dinamici](basic-and-dynamic-disks.md).

La creazione di più partizioni in un disco consente l'aspetto di dischi rigidi separati. Un sistema con un disco rigido con una partizione, ad esempio, contiene un singolo volume, designato dal sistema come unità C. Un sistema con un disco rigido con due partizioni contiene in genere unità C e D. La presenza di più partizioni in un disco rigido può semplificare la gestione del sistema, ad esempio per organizzare i file o per supportare più utenti.

Il primo settore fisico in un disco di base contiene una struttura di dati nota come MBR (master boot record). Il MBR contiene gli elementi seguenti:

-   Un programma di avvio (dimensioni fino a 442 byte)
-   Firma del disco (un numero univoco di 4 byte)
-   Una tabella di partizione (fino a quattro voci)
-   Indicatore di fine MBR (always 0x55AA)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla gestione dei volumi](about-volume-management.md)
</dt> <dt>

[Dischi di base e dinamici](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



