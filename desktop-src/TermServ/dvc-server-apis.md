---
title: API del server DVC
description: Le API del server del canale virtuale dinamico (DVC) vengono implementate dal server Connessione Desktop remoto (RDC) della connessione.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399597"
---
# <a name="dvc-server-apis"></a><span data-ttu-id="21671-103">API del server DVC</span><span class="sxs-lookup"><span data-stu-id="21671-103">DVC Server APIs</span></span>

<span data-ttu-id="21671-104">Le API del server del canale virtuale dinamico (DVC) vengono implementate dal server Connessione Desktop remoto (RDC) della connessione.</span><span class="sxs-lookup"><span data-stu-id="21671-104">The dynamic virtual channel (DVC) server APIs are implemented by the Remote Desktop Connection (RDC) server of the connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="21671-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="21671-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="21671-106">**IWTSServerChannel**</span><span class="sxs-lookup"><span data-stu-id="21671-106">**IWTSServerChannel**</span></span>](iwtsserverchannel.md)
</dt> <dd>

<span data-ttu-id="21671-107">Questa interfaccia non è supportata.</span><span class="sxs-lookup"><span data-stu-id="21671-107">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="21671-108">**IWTSServerChannelManager**</span><span class="sxs-lookup"><span data-stu-id="21671-108">**IWTSServerChannelManager**</span></span>](iwtsserverchannelmanager.md)
</dt> <dd>

<span data-ttu-id="21671-109">Questa interfaccia non è supportata.</span><span class="sxs-lookup"><span data-stu-id="21671-109">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="21671-110">**TPriority**</span><span class="sxs-lookup"><span data-stu-id="21671-110">**TPriority**</span></span>](tpriority.md)
</dt> <dd>

<span data-ttu-id="21671-111">Questa enumerazione non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="21671-111">This enumeration is not used.</span></span>

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a><span data-ttu-id="21671-112">Modifiche al comportamento per altre API del server</span><span class="sxs-lookup"><span data-stu-id="21671-112">Changes in Behavior for Other Server APIs</span></span>

-   <span data-ttu-id="21671-113">L'API server è stata estesa con una chiamata aggiuntiva che apre un canale virtuale dinamico (DVC).</span><span class="sxs-lookup"><span data-stu-id="21671-113">The server API has been extended with an additional call which opens a dynamic virtual channel (DVC).</span></span> <span data-ttu-id="21671-114">La chiamata aggiuntiva viene eseguita utilizzando la funzione [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .</span><span class="sxs-lookup"><span data-stu-id="21671-114">The additional call is made using the [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) function.</span></span>
-   [<span data-ttu-id="21671-115">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="21671-115">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    <span data-ttu-id="21671-116">Quando si usa questa API con DVC, viene sempre anteposto i dati letti con [**l' \_ \_ intestazione di Channel PDU**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span><span class="sxs-lookup"><span data-stu-id="21671-116">When using this API with DVC, it will always prepend the data read with [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span></span> <span data-ttu-id="21671-117">Ciò significa che qualsiasi operazione di lettura deve essere eseguita con almeno il blocco di dati della **\_ \_ lunghezza PDU del canale** passato come buffer di input.</span><span class="sxs-lookup"><span data-stu-id="21671-117">This means that any read must be done with at least the **CHANNEL\_PDU\_LENGTH** data block passed as the input buffer.</span></span>

-   [<span data-ttu-id="21671-118">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="21671-118">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    <span data-ttu-id="21671-119">Se l'handle di file per DVC viene recuperato chiamando [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) con il parametro *WTSVirtualFileHandle*, verrà applicata la stessa regola.</span><span class="sxs-lookup"><span data-stu-id="21671-119">If the file handle to the DVC is retrieved by calling [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) with parameter *WTSVirtualFileHandle*, the same rule will apply.</span></span> <span data-ttu-id="21671-120">Tutte le letture includeranno [**l' \_ \_ intestazione PDU del canale**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)e il buffer di lettura deve avere una dimensione di lunghezza minima della **\_ PDU \_ del canale** .</span><span class="sxs-lookup"><span data-stu-id="21671-120">All reads will include the [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), and the read buffer has to be at least **CHANNEL\_PDU\_LENGTH** size.</span></span>

 

 