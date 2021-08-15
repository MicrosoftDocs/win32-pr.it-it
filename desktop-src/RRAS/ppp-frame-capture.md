---
title: Scrittura di un driver per acquisire frame PPP
description: Questo documento illustra come sviluppare un driver in grado di acquisire i frame PPP in Windows Vista prima che siano compressi/crittografati nel percorso di invio o dopo che vengono decompressi/decrittografati nel percorso di ricezione.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b769a07811980b20ab076f60cc1e4fd7d9aa227b8eecfa44e71089bc949d0de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789689"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a>Scrittura di un driver per acquisire frame PPP

Quando i frame Point-to-Point Protocol (PPP) vengono inviati tramite un tunnel PPTP (Point-to-Point Tunneling Protocol) con crittografia attivata o tramite un tunnel L2TP (Layer 2 Tunneling Protocol) che usa IPSec per la crittografia, la tipica utilità di acquisizione di frame PPP può acquisire solo frame PPP con un campo di identità del protocollo crittografato. Questo documento illustra come sviluppare un driver in grado di acquisire i frame PPP in Windows Vista prima che siano compressi/crittografati nel percorso di invio o dopo che vengono decompressi/decrittografati nel percorso di ricezione.

1.  Scrivere un driver del protocollo NDIS. Per informazioni dettagliate, vedere NDIS 6.0 Protocol Drivers (Driver del protocollo [NDIS 6.0)](https://msdn.microsoft.com/library/ms795570.aspx) o [NDIS Protocol Drivers (NDIS 5.1) (Driver del protocollo NDIS NDIS 5.1).](https://msdn.microsoft.com/library/ms801145.aspx)
2.  Installare il driver con un'identità hardware "ms \_ netmon". Per istruzioni dettagliate su come installare il driver con un'identità hardware specifica, vedere [la sezione Modelli INF.](https://msdn.microsoft.com/library/ms794357.aspx)
    > [!Note]  
    > Ogni Windows Vista consente l'installazione di una sola entità driver con l'identità hardware "ms \_ netmon". Per installare un altro driver con questa identità, è necessario disinstallare il primo driver. Un driver installato senza usare l'identità hardware "ms netmon" non può eseguire \_ l'associazione necessaria per acquisire i frame PPP.

     

3.  Il driver del protocollo deve specificare "ndiswanbh" come interfaccia di associazione per l'acquisizione di frame PPP. Per istruzioni dettagliate, vedere [Specifica delle interfacce di associazione.](https://msdn.microsoft.com/library/aa937923.aspx)
4.  L'implementazione di [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) nel driver deve supportare "NdisMediumWan" come parte della matrice media, in modo che possa aprire il bordo del miniport ndiswanbh usando la funzione [NdisOpenAdapter.](https://msdn.microsoft.com/library/ms804862.aspx)
5.  Se la funzione [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) viene chiamata con stato NDIS STATUS SUCCESS, il driver del protocollo deve impostare \_ \_ [l'OID OID \_ GEN CURRENT PACKET \_ \_ \_ FILTER](https://msdn.microsoft.com/library/bb314089.aspx) con i flag [NDIS \_ PACKET TYPE \_ \_ PROMISCUOUS](https://msdn.microsoft.com/library/bb314089.aspx) e [NDIS \_ PACKET TYPE ALL \_ \_ \_ LOCAL](https://msdn.microsoft.com/library/bb314089.aspx) su questa associazione. Al termine, il driver del protocollo riceverà i frame PPP decrittografati dal livello di framing PPP nella relativa [funzione ProtocolReceive.](https://msdn.microsoft.com/library/ms797274.aspx)

> [!Note]  
> Queste informazioni si applicano solo ai driver in un computer Windows Vista.

 

 

 




