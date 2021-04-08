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
# <a name="writing-a-driver-to-capture-ppp-frames"></a><span data-ttu-id="16451-103">Scrittura di un driver per l'acquisizione di frame PPP</span><span class="sxs-lookup"><span data-stu-id="16451-103">Writing a Driver to Capture PPP Frames</span></span>

<span data-ttu-id="16451-104">Quando vengono inviati i frame Point-to-Point Protocol (PPP) tramite un tunnel PPTP (Point-to-Point Tunneling Protocol) con la crittografia attivata o tramite un tunnel L2TP (Layer 2 Tunneling Protocol) che utilizza IPSec per la crittografia, la tipica utilità di acquisizione di frame PPP può acquisire solo frame PPP con un campo di identità del protocollo crittografato.</span><span class="sxs-lookup"><span data-stu-id="16451-104">When Point-to-Point Protocol (PPP) frames are sent through a Point-to-Point Tunneling Protocol (PPTP) tunnel with encryption turned on, or through a Layer 2 Tunneling Protocol (L2TP) tunnel that uses IPSec for encryption, the typical PPP frame capture utility can only capture PPP frames that have an encrypted protocol identity field.</span></span> <span data-ttu-id="16451-105">In questo documento viene illustrato come sviluppare un driver in grado di acquisire frame PPP in Windows Vista prima che vengano compressi/crittografati nel percorso di trasmissione o dopo che sono stati decompressi/decrittografati nel percorso di ricezione.</span><span class="sxs-lookup"><span data-stu-id="16451-105">This document explains how to develop a driver that can capture PPP frames in Windows Vista before they are compressed/encrypted in the send path or after they are decompressed/decrypted in the receive path.</span></span>

1.  <span data-ttu-id="16451-106">Scrivere un driver del protocollo NDIS.</span><span class="sxs-lookup"><span data-stu-id="16451-106">Write an NDIS protocol driver.</span></span> <span data-ttu-id="16451-107">Per informazioni dettagliate, vedere [driver del protocollo ndis 6,0](https://msdn.microsoft.com/library/ms795570.aspx) o [driver del protocollo ndis (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).</span><span class="sxs-lookup"><span data-stu-id="16451-107">For details, see [NDIS 6.0 Protocol Drivers](https://msdn.microsoft.com/library/ms795570.aspx) or [NDIS Protocol Drivers (NDIS 5.1)](https://msdn.microsoft.com/library/ms801145.aspx).</span></span>
2.  <span data-ttu-id="16451-108">Installare il driver con un'identità hardware "MS \_ Netmon".</span><span class="sxs-lookup"><span data-stu-id="16451-108">Install the driver with a hardware identity of "ms\_netmon".</span></span> <span data-ttu-id="16451-109">Per istruzioni dettagliate su come installare il driver con un'identità hardware specifica, vedere la [sezione modelli inf](https://msdn.microsoft.com/library/ms794357.aspx).</span><span class="sxs-lookup"><span data-stu-id="16451-109">For detailed instructions on how to install the driver with a specific hardware identity, see [INF Models Section](https://msdn.microsoft.com/library/ms794357.aspx).</span></span>
    > [!Note]  
    > <span data-ttu-id="16451-110">Ogni computer Windows Vista consente l'installazione di una sola entità driver con l' \_ identità hardware "MS Netmon".</span><span class="sxs-lookup"><span data-stu-id="16451-110">Each Windows Vista machine permits the installation of only one driver entity that has the "ms\_netmon" hardware identity.</span></span> <span data-ttu-id="16451-111">Per installare un altro driver con questa identità, è necessario disinstallare il primo driver.</span><span class="sxs-lookup"><span data-stu-id="16451-111">To install another driver with this identity, the first driver must be uninstalled.</span></span> <span data-ttu-id="16451-112">Un driver installato senza utilizzare l'identità hardware "MS \_ Netmon" non può eseguire l'associazione necessaria per acquisire i frame PPP.</span><span class="sxs-lookup"><span data-stu-id="16451-112">A driver that is installed without using the "ms\_netmon" hardware identity cannot perform the binding needed to capture PPP frames.</span></span>

     

3.  <span data-ttu-id="16451-113">Il driver di protocollo deve specificare "NDISWANBH" come interfaccia di associazione per l'acquisizione di frame PPP.</span><span class="sxs-lookup"><span data-stu-id="16451-113">The protocol driver should specify "ndiswanbh" as the binding interface for capturing PPP frames.</span></span> <span data-ttu-id="16451-114">Per istruzioni dettagliate, vedere [specifica delle interfacce di binding](https://msdn.microsoft.com/library/aa937923.aspx).</span><span class="sxs-lookup"><span data-stu-id="16451-114">For detailed instructions, see [Specifying Binding Interfaces](https://msdn.microsoft.com/library/aa937923.aspx).</span></span>
4.  <span data-ttu-id="16451-115">L'implementazione di [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) nel driver deve supportare "NdisMediumWan" come parte dell'array medio, in modo da poter aprire il bordo di NDISWANBH miniport usando la funzione [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) .</span><span class="sxs-lookup"><span data-stu-id="16451-115">The [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) implementation in the driver should support "NdisMediumWan" as a part of the medium array, so that it can open the ndiswanbh miniport edge using the [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) function.</span></span>
5.  <span data-ttu-id="16451-116">Se la funzione [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) viene chiamata con lo stato \_ NDIS \_ Success status, il driver di protocollo deve impostare l'OID del filtro dei pacchetti per la [ \_ generazione \_ \_ \_ OID](https://msdn.microsoft.com/library/bb314089.aspx) con i flag [tipo di \_ pacchetto NDIS \_ \_ promiscuo](https://msdn.microsoft.com/library/bb314089.aspx) e [NDIS tipo di \_ pacchetto tutti i \_ \_ \_ locali](https://msdn.microsoft.com/library/bb314089.aspx) su questa associazione.</span><span class="sxs-lookup"><span data-stu-id="16451-116">If the [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) function is called with status NDIS\_STATUS\_SUCCESS, the protocol driver should set the [OID\_GEN\_CURRENT\_PACKET\_FILTER](https://msdn.microsoft.com/library/bb314089.aspx) OID with the flags [NDIS\_PACKET\_TYPE\_PROMISCUOUS](https://msdn.microsoft.com/library/bb314089.aspx) and [NDIS\_PACKET\_TYPE\_ALL\_LOCAL](https://msdn.microsoft.com/library/bb314089.aspx) over this binding.</span></span> <span data-ttu-id="16451-117">Al termine di questa operazione, il driver di protocollo riceverà i frame PPP decrittografati dal livello di framing PPP nella funzione [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) .</span><span class="sxs-lookup"><span data-stu-id="16451-117">Once this is done, the protocol driver will receive the decrypted PPP frames from the PPP framing layer in its [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) function.</span></span>

> [!Note]  
> <span data-ttu-id="16451-118">Queste informazioni si applicano solo ai driver in un computer con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16451-118">This information only applies to drivers on a Windows Vista machine.</span></span>

 

 

 




