---
title: Struttura ORPC_DBG_BUFFER
description: La \_ struttura del \_ buffer dbg ORPC è il formato del buffer usato per i dati RPC con marshalling nei metodi dell'interfaccia IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- COM struttura ORPC_DBG_BUFFER
- Puntatore a struttura PORPC_DBG_BUFFER COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301283"
---
# <a name="orpc_dbg_buffer-structure"></a><span data-ttu-id="cd87d-105">\_Struttura del \_ buffer dbg ORPC</span><span class="sxs-lookup"><span data-stu-id="cd87d-105">ORPC\_DBG\_BUFFER structure</span></span>

<span data-ttu-id="cd87d-106">La struttura del **\_ \_ buffer dbg ORPC** è il formato del buffer usato per i dati RPC con marshalling nei metodi dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="cd87d-106">The **ORPC\_DBG\_BUFFER** structure is the buffer format used to marshalled RPC data to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd87d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd87d-107">Syntax</span></span>


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a><span data-ttu-id="cd87d-108">Members</span><span class="sxs-lookup"><span data-stu-id="cd87d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd87d-109">**alwaysOrSometimes**</span><span class="sxs-lookup"><span data-stu-id="cd87d-109">**alwaysOrSometimes**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-110">Valore che controlla la generazione del debugger.</span><span class="sxs-lookup"><span data-stu-id="cd87d-110">A value that controls debugger spawning.</span></span> <span data-ttu-id="cd87d-111">**alwaysOrSometimes** può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd87d-111">**alwaysOrSometimes** can be one of the following values:</span></span>



| <span data-ttu-id="cd87d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="cd87d-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="cd87d-113">Significato</span><span class="sxs-lookup"><span data-stu-id="cd87d-113">Meaning</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <span data-ttu-id="cd87d-114"><dt>**ORPC \_ DEBUG \_ sempre**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="cd87d-114"><dt>**ORPC\_DEBUG\_ALWAYS**</dt> <dt>0x00000000</dt></span></span> </dl>                              | <span data-ttu-id="cd87d-115">Se impostato, COM genererà sempre la notifica del client o del server sul ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cd87d-115">If set, COM will always raise the client or server notification on the receiver.</span></span><br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <span data-ttu-id="cd87d-116"><dt>**ORPC \_ DEBUG \_ se l' \_ hook è \_ abilitato**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="cd87d-116"><dt>**ORPC\_DEBUG\_IF\_HOOK\_ENABLED**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="cd87d-117">Se impostato, COM genererà solo la notifica client o server sul ricevitore se è stato abilitato il debug COM chiamando [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in tale processo con **FTrace** impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="cd87d-117">If set, COM will only raise the client or server notification on the receiver if COM debugging has been enabled by calling [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in that process with **fTrace** set to **TRUE**.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="cd87d-118">**verMajor**</span><span class="sxs-lookup"><span data-stu-id="cd87d-118">**verMajor**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-119">Numero di versione principale della specifica del formato dati.</span><span class="sxs-lookup"><span data-stu-id="cd87d-119">The major version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="cd87d-120">**VersioneSecondaria**</span><span class="sxs-lookup"><span data-stu-id="cd87d-120">**verMinor**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-121">Numero della versione secondaria della specifica del formato dati.</span><span class="sxs-lookup"><span data-stu-id="cd87d-121">The minor version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="cd87d-122">**cbRemaining**</span><span class="sxs-lookup"><span data-stu-id="cd87d-122">**cbRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-123">Numero di byte, inclusi **cbRemaining**, che seguono la struttura.</span><span class="sxs-lookup"><span data-stu-id="cd87d-123">The number of bytes, inclusive of **cbRemaining**, that follow in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd87d-124">**guidSemantic**</span><span class="sxs-lookup"><span data-stu-id="cd87d-124">**guidSemantic**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-125">GUID che determina i membri dell'Unione presenti sotto.</span><span class="sxs-lookup"><span data-stu-id="cd87d-125">A GUID that determines which members of the union are present below.</span></span> <span data-ttu-id="cd87d-126">**guidSemantic** può assumere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd87d-126">**guidSemantic** can take one of the following values:</span></span>



| <span data-ttu-id="cd87d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="cd87d-127">Value</span></span>                                                                                                           | <span data-ttu-id="cd87d-128">Significato</span><span class="sxs-lookup"><span data-stu-id="cd87d-128">Meaning</span></span>                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd87d-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span><span class="sxs-lookup"><span data-stu-id="cd87d-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span></span> </dl> | <span data-ttu-id="cd87d-130">Determina se il debugger deve eseguire l'esecuzione singola.</span><span class="sxs-lookup"><span data-stu-id="cd87d-130">Determines if single stepping is to be performed by the debugger.</span></span> <span data-ttu-id="cd87d-131">Di seguito è disponibile solo il membro **fStopOnOtherSide** dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="cd87d-131">Only the **fStopOnOtherSide** member of the union is present below.</span></span><br/>                                             |
| <dl> <span data-ttu-id="cd87d-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="cd87d-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="cd87d-133">Determina se i dati e i codici operativi di debug RPC vengono passati al ricevitore.</span><span class="sxs-lookup"><span data-stu-id="cd87d-133">Determines if RPC marshalled data and debugging opcodes are passed to the receiver.</span></span> <span data-ttu-id="cd87d-134">Tutti i membri dell'Unione sono presenti di seguito, ad eccezione di **fStopOnOtherSide**.</span><span class="sxs-lookup"><span data-stu-id="cd87d-134">All of the members of the union are present below with the exception of **fStopOnOtherSide**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd87d-135">**fStopOnOtherSide**</span><span class="sxs-lookup"><span data-stu-id="cd87d-135">**fStopOnOtherSide**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-136">Se il valore è **true**, il debugger esegue un'istruzione/routine singola e deve uscire dal server e continuare l'esecuzione una volta raggiunto l'altro lato.</span><span class="sxs-lookup"><span data-stu-id="cd87d-136">If **TRUE**, single stepping is performed by the debugger and it should step out of the server and continue execution once the other side is reached.</span></span> <span data-ttu-id="cd87d-137">In caso contrario, l'esecuzione di un singolo passo non viene eseguita e l'esecuzione del debugger si interrompe sull'altro lato.</span><span class="sxs-lookup"><span data-stu-id="cd87d-137">Otherwise, single stepping is not performed and debugger execution stops on the other side.</span></span>

</dd> <dt>

<span data-ttu-id="cd87d-138">**wDebuggingOpCode**</span><span class="sxs-lookup"><span data-stu-id="cd87d-138">**wDebuggingOpCode**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-139">Valore che consente di specificare una di una serie di operazioni.</span><span class="sxs-lookup"><span data-stu-id="cd87d-139">A value that allows for one of a series of operations to be specified.</span></span> <span data-ttu-id="cd87d-140">**wDebuggingOpCode** può assumere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd87d-140">**wDebuggingOpCode** can take one of the following values:</span></span>



| <span data-ttu-id="cd87d-141">Valore</span><span class="sxs-lookup"><span data-stu-id="cd87d-141">Value</span></span>                                                                             | <span data-ttu-id="cd87d-142">Significato</span><span class="sxs-lookup"><span data-stu-id="cd87d-142">Meaning</span></span>                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd87d-143"><dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="cd87d-143"><dt>0x0000</dt></span></span> </dl> | <span data-ttu-id="cd87d-144">Nessuna operazione.</span><span class="sxs-lookup"><span data-stu-id="cd87d-144">No operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="cd87d-145"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="cd87d-145"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="cd87d-146">Se impostata, la semantica del singolo passaggio è identica a **fStopOnOtherSide** quando è impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="cd87d-146">If set, single step semantics are identical to **fStopOnOtherSide** when set to **TRUE**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd87d-147">**cExtent**</span><span class="sxs-lookup"><span data-stu-id="cd87d-147">**cExtent**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-148">Imbottitura.</span><span class="sxs-lookup"><span data-stu-id="cd87d-148">Padding.</span></span> <span data-ttu-id="cd87d-149">Non usare.</span><span class="sxs-lookup"><span data-stu-id="cd87d-149">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="cd87d-150">**padding**</span><span class="sxs-lookup"><span data-stu-id="cd87d-150">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-151">Imbottitura.</span><span class="sxs-lookup"><span data-stu-id="cd87d-151">Padding.</span></span> <span data-ttu-id="cd87d-152">Non usare.</span><span class="sxs-lookup"><span data-stu-id="cd87d-152">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="cd87d-153">**CB**</span><span class="sxs-lookup"><span data-stu-id="cd87d-153">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-154">Dimensioni in byte dei dati in **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="cd87d-154">The size, in bytes of the data in **rgbData**.</span></span>

</dd> <dt>

<span data-ttu-id="cd87d-155">**guidExtent**</span><span class="sxs-lookup"><span data-stu-id="cd87d-155">**guidExtent**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-156">**GUID** che determina il tipo di dati in **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="cd87d-156">A **GUID** that determines the type of data in **rgbData**.</span></span> <span data-ttu-id="cd87d-157">**guidExtent** può assumere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd87d-157">**guidExtent** can take one of the following values:</span></span>



| <span data-ttu-id="cd87d-158">Valore</span><span class="sxs-lookup"><span data-stu-id="cd87d-158">Value</span></span>                                                                                                           | <span data-ttu-id="cd87d-159">Significato</span><span class="sxs-lookup"><span data-stu-id="cd87d-159">Meaning</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="cd87d-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="cd87d-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="cd87d-161">**rgbData** è un puntatore a interfaccia con marshalling.</span><span class="sxs-lookup"><span data-stu-id="cd87d-161">**rgbData** is a marshalled interface pointer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd87d-162">**rgbData**</span><span class="sxs-lookup"><span data-stu-id="cd87d-162">**rgbData**</span></span>
</dt> <dd>

<span data-ttu-id="cd87d-163">Buffer di **byte** utilizzato per passare i dati com con marshalling RPC tra i debugger client e server.</span><span class="sxs-lookup"><span data-stu-id="cd87d-163">A **BYTE** buffer used to pass RPC marshalled COM data between the client and server debuggers.</span></span> <span data-ttu-id="cd87d-164">Il contenuto di **rgbData** è determinato dal **GUID** in **guidExtent**.</span><span class="sxs-lookup"><span data-stu-id="cd87d-164">The contents of **rgbData** are determined by the **GUID** in **guidExtent**.</span></span>



| <span data-ttu-id="cd87d-165">Valore guidExtent</span><span class="sxs-lookup"><span data-stu-id="cd87d-165">guidExtent Value</span></span>                     | <span data-ttu-id="cd87d-166">contenuto di rgbData</span><span class="sxs-lookup"><span data-stu-id="cd87d-166">rgbData contents</span></span>                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd87d-167">53199051-57EB-11ce-A964-00AA006C3706</span><span class="sxs-lookup"><span data-stu-id="cd87d-167">53199051-57EB-11ce-A964-00AA006C3706</span></span> | <span data-ttu-id="cd87d-168">Puntatore a un'interfaccia con marshalling risultante dalla chiamata a [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="cd87d-168">A marshalled interface pointer that results from calling [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span></span> <span data-ttu-id="cd87d-169">Il puntatore di marshalling viene convertito nel puntatore a interfaccia corrispondente utilizzando [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="cd87d-169">The marshalled pointer is converted into its corresponding interface pointer using [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd87d-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd87d-170">Remarks</span></span>

<span data-ttu-id="cd87d-171">I membri di questa struttura hanno un allineamento a 1 byte e vengono sempre trasmessi nell'ordine dei byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="cd87d-171">This members of this structure have 1-byte alignment and are always transmitted in little-endian byte order.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd87d-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd87d-172">Requirements</span></span>



| <span data-ttu-id="cd87d-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd87d-173">Requirement</span></span> | <span data-ttu-id="cd87d-174">Valore</span><span class="sxs-lookup"><span data-stu-id="cd87d-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cd87d-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd87d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="cd87d-176">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd87d-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="cd87d-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd87d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="cd87d-178">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd87d-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cd87d-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd87d-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd87d-180"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="cd87d-180"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd87d-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd87d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd87d-182">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="cd87d-182">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="cd87d-183">**\_argomenti init \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="cd87d-183">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="cd87d-184">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="cd87d-184">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="cd87d-185">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="cd87d-185">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





