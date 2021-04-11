---
title: Struttura ORPC_DBG_ALL
description: La \_ struttura ORPC dbg \_ All viene utilizzata per passare parametri ai metodi dell'interfaccia IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- COM struttura ORPC_DBG_ALL
- Puntatore a struttura LPORPC_DBG_ALL COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119366"
---
# <a name="orpc_dbg_all-structure"></a><span data-ttu-id="5e65c-105">\_Struttura ORPC dbg \_ All</span><span class="sxs-lookup"><span data-stu-id="5e65c-105">ORPC\_DBG\_ALL structure</span></span>

<span data-ttu-id="5e65c-106">La struttura **ORPC \_ dbg \_ All** viene utilizzata per passare parametri ai metodi dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-106">The **ORPC\_DBG\_ALL** structure is used to pass parameters to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="5e65c-107">Ogni metodo dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) utilizza una combinazione diversa dei membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e65c-107">Each method of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface uses a different combination of the members below.</span></span> <span data-ttu-id="5e65c-108">Se un membro non è indicato come usato da un metodo, non è definito quando viene passato al metodo.</span><span class="sxs-lookup"><span data-stu-id="5e65c-108">If a member is not indicated as used by a method, it is undefined when passed to that method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5e65c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e65c-109">Syntax</span></span>


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a><span data-ttu-id="5e65c-110">Members</span><span class="sxs-lookup"><span data-stu-id="5e65c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5e65c-111">**pSignature**</span><span class="sxs-lookup"><span data-stu-id="5e65c-111">**pSignature**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-112">Puntatore a un buffer di **byte** che contiene:</span><span class="sxs-lookup"><span data-stu-id="5e65c-112">A pointer to a **BYTE** buffer that contains:</span></span>

-   <span data-ttu-id="5e65c-113">Primi quattro byte: caratteri ASCII "MARB" in ordine di memoria crescente.</span><span class="sxs-lookup"><span data-stu-id="5e65c-113">First four bytes: the ASCII characters "MARB" in increasing memory order.</span></span>
-   <span data-ttu-id="5e65c-114">Successivi 16 byte: **GUID** che identifica la notifica chiamata.</span><span class="sxs-lookup"><span data-stu-id="5e65c-114">Next 16 bytes: A **GUID** that identifies the notification being called.</span></span> <span data-ttu-id="5e65c-115">Contiene uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="5e65c-115">It contains one of the following:</span></span>
    1.  <span data-ttu-id="5e65c-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="5e65c-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span></span>
    2.  <span data-ttu-id="5e65c-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="5e65c-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):DA45F3E0-9673-101A-B07B-00DD01113F11</span></span>
    3.  <span data-ttu-id="5e65c-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="5e65c-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11</span></span>
    4.  <span data-ttu-id="5e65c-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="5e65c-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11</span></span>
    5.  <span data-ttu-id="5e65c-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="5e65c-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11</span></span>
    6.  <span data-ttu-id="5e65c-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="5e65c-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11</span></span>
-   <span data-ttu-id="5e65c-122">Successivi quattro byte: riservati per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5e65c-122">Next four-bytes: Reserved for future use.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-123">Utilizzato da tutti i metodi dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-123">Used by all methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-124">**pMessage**</span><span class="sxs-lookup"><span data-stu-id="5e65c-124">**pMessage**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-125">Puntatore a una struttura [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) che contiene informazioni di marshalling dei dati RPC.</span><span class="sxs-lookup"><span data-stu-id="5e65c-125">A pointer to an [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) structure that contains RPC data marshalling information.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-126">Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-126">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-127">**REFIID**</span><span class="sxs-lookup"><span data-stu-id="5e65c-127">**refiid**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-128">Puntatore all'IID dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-128">A pointer to the IID of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-129">Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-129">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-130">**pChannel**</span><span class="sxs-lookup"><span data-stu-id="5e65c-130">**pChannel**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-131">Puntatore all'interfaccia [**Metodo IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) dell'implementazione del canale RPC com sul server.</span><span class="sxs-lookup"><span data-stu-id="5e65c-131">A pointer to the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface of the COM RPC channel implementation on the server.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-132">Utilizzato dai metodi [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-132">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-133">**pUnkProxyMgr**</span><span class="sxs-lookup"><span data-stu-id="5e65c-133">**pUnkProxyMgr**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-134">Puntatore all'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) dell'oggetto che ha richiesto la chiamata al debugger.</span><span class="sxs-lookup"><span data-stu-id="5e65c-134">A pointer to the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the object involved in this debugger invocation.</span></span> <span data-ttu-id="5e65c-135">Può essere **null**, tuttavia, riduce la funzionalità del debugger.</span><span class="sxs-lookup"><span data-stu-id="5e65c-135">May be **NULL**, however, this reduces debugger functionality.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-136">Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)e [**ClientNotify**](iorpcdebugnotify-clientnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-136">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), and [**ClientNotify**](iorpcdebugnotify-clientnotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-137">**pInterface**</span><span class="sxs-lookup"><span data-stu-id="5e65c-137">**pInterface**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-138">Puntatore all'interfaccia COM del metodo che verrà richiamato da questa RPC.</span><span class="sxs-lookup"><span data-stu-id="5e65c-138">A pointer to the COM interface of the method that will be invoked by this RPC.</span></span> <span data-ttu-id="5e65c-139">Non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5e65c-139">Must not be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-140">Utilizzato dai metodi [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-140">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-141">**pUnkObject**</span><span class="sxs-lookup"><span data-stu-id="5e65c-141">**pUnkObject**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-142">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5e65c-142">Must be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-143">Utilizzato dai metodi [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-143">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-144">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e65c-144">**hresult**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-145">Le modifiche a scopo di questo membro per ognuna delle notifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="5e65c-145">This member's purpose changes for each of the notifications below:</span></span>

<span data-ttu-id="5e65c-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): numero di byte che il debugger client trasmetterà al debugger del server.</span><span class="sxs-lookup"><span data-stu-id="5e65c-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="5e65c-147">Se è zero, non è necessario trasmettere alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="5e65c-147">If zero, no information need be transmitted.</span></span>

<span data-ttu-id="5e65c-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): **HRESULT** dell'ultima RPC.</span><span class="sxs-lookup"><span data-stu-id="5e65c-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): the **HRESULT** of the last RPC.</span></span>

<span data-ttu-id="5e65c-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): numero di byte che il debugger client trasmetterà al debugger del server.</span><span class="sxs-lookup"><span data-stu-id="5e65c-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="5e65c-150">Se è zero, non è necessario trasmettere alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="5e65c-150">If zero, no information need be transmitted.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-151">Utilizzato dai metodi [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)e [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-151">Used by the [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), and [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-152">**pvBuffer**</span><span class="sxs-lookup"><span data-stu-id="5e65c-152">**pvBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-153">Puntatore a una struttura [**di \_ \_ buffer di ORPC dbg**](orpc-dbg-buffer.md) che contiene le informazioni di debug con marshalling RPC.</span><span class="sxs-lookup"><span data-stu-id="5e65c-153">A pointer to an [**ORPC\_DBG\_BUFFER**](orpc-dbg-buffer.md) structure that contains the RPC marshalled debug information.</span></span> <span data-ttu-id="5e65c-154">Non è definito se **cbBuffer** è zero.</span><span class="sxs-lookup"><span data-stu-id="5e65c-154">Is undefined if **cbBuffer** is zero.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-155">Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-155">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-156">**cbBuffer**</span><span class="sxs-lookup"><span data-stu-id="5e65c-156">**cbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-157">Lunghezza, in byte, dei dati a cui punta **pvBuffer**.</span><span class="sxs-lookup"><span data-stu-id="5e65c-157">The length, in bytes, of the data pointed to by **pvBuffer**.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-158">Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-158">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-159">**lpcbBuffer**</span><span class="sxs-lookup"><span data-stu-id="5e65c-159">**lpcbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-160">Numero di byte che il debugger client trasmetterà al debugger del server.</span><span class="sxs-lookup"><span data-stu-id="5e65c-160">The number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="5e65c-161">Se è zero, non è necessario trasmettere alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="5e65c-161">If zero, no information need be transmitted.</span></span> <span data-ttu-id="5e65c-162">Questo valore sostituisce il valore restituito in **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5e65c-162">This value supersedes the value returned in **hresult**.</span></span>

> [!Note]
>
> <span data-ttu-id="5e65c-163">Utilizzato dai metodi [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="5e65c-163">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e65c-164">**riservati**</span><span class="sxs-lookup"><span data-stu-id="5e65c-164">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="5e65c-165">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5e65c-165">Reserved.</span></span> <span data-ttu-id="5e65c-166">Non usare.</span><span class="sxs-lookup"><span data-stu-id="5e65c-166">Do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e65c-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e65c-167">Requirements</span></span>



| <span data-ttu-id="5e65c-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e65c-168">Requirement</span></span> | <span data-ttu-id="5e65c-169">Valore</span><span class="sxs-lookup"><span data-stu-id="5e65c-169">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5e65c-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e65c-170">Minimum supported client</span></span><br/> | <span data-ttu-id="5e65c-171">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e65c-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="5e65c-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e65c-172">Minimum supported server</span></span><br/> | <span data-ttu-id="5e65c-173">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e65c-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5e65c-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e65c-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e65c-175"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="5e65c-175"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e65c-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e65c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e65c-177">**\_buffer dbg \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="5e65c-177">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="5e65c-178">**\_argomenti init \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="5e65c-178">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="5e65c-179">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="5e65c-179">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="5e65c-180">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="5e65c-180">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

