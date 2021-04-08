---
title: Scrittura di un driver per l'acquisizione di frame PPP
description: In questo documento viene illustrato come sviluppare un driver in grado di acquisire frame PPP in Windows Vista prima che vengano compressi/crittografati nel percorso di trasmissione o dopo che sono stati decompressi/decrittografati nel percorso di ricezione.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046359"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a>Scrittura di un driver per l'acquisizione di frame PPP

Quando vengono inviati i frame Point-to-Point Protocol (PPP) tramite un tunnel PPTP (Point-to-Point Tunneling Protocol) con la crittografia attivata o tramite un tunnel L2TP (Layer 2 Tunneling Protocol) che utilizza IPSec per la crittografia, la tipica utilità di acquisizione di frame PPP può acquisire solo frame PPP con un campo di identità del protocollo crittografato. In questo documento viene illustrato come sviluppare un driver in grado di acquisire frame PPP in Windows Vista prima che vengano compressi/crittografati nel percorso di trasmissione o dopo che sono stati decompressi/decrittografati nel percorso di ricezione.

1.  Scrivere un driver del protocollo NDIS. Per informazioni dettagliate, vedere [driver del protocollo ndis 6,0](https://msdn.microsoft.com/library/ms795570.aspx) o [driver del protocollo ndis (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).
2.  Installare il driver con un'identità hardware "MS \_ Netmon". Per istruzioni dettagliate su come installare il driver con un'identità hardware specifica, vedere la [sezione modelli inf](https://msdn.microsoft.com/library/ms794357.aspx).
    > [!Note]  
    > Ogni computer Windows Vista consente l'installazione di una sola entità driver con l' \_ identità hardware "MS Netmon". Per installare un altro driver con questa identità, è necessario disinstallare il primo driver. Un driver installato senza utilizzare l'identità hardware "MS \_ Netmon" non può eseguire l'associazione necessaria per acquisire i frame PPP.

     

3.  Il driver di protocollo deve specificare "NDISWANBH" come interfaccia di associazione per l'acquisizione di frame PPP. Per istruzioni dettagliate, vedere [specifica delle interfacce di binding](https://msdn.microsoft.com/library/aa937923.aspx).
4.  L'implementazione di [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) nel driver deve supportare "NdisMediumWan" come parte dell'array medio, in modo da poter aprire il bordo di NDISWANBH miniport usando la funzione [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) .
5.  Se la funzione [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) viene chiamata con lo stato \_ NDIS \_ Success status, il driver di protocollo deve impostare l'OID del filtro dei pacchetti per la [ \_ generazione \_ \_ \_ OID](https://msdn.microsoft.com/library/bb314089.aspx) con i flag [tipo di \_ pacchetto NDIS \_ \_ promiscuo](https://msdn.microsoft.com/library/bb314089.aspx) e [NDIS tipo di \_ pacchetto tutti i \_ \_ \_ locali](https://msdn.microsoft.com/library/bb314089.aspx) su questa associazione. Al termine di questa operazione, il driver di protocollo riceverà i frame PPP decrittografati dal livello di framing PPP nella funzione [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) .

> [!Note]  
> Queste informazioni si applicano solo ai driver in un computer con Windows Vista.

 

 

 




