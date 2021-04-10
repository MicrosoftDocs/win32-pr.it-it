---
title: Metodo IMsTscAxEvents OnRemoteProgramResult
description: Chiamato quando un programma RemoteApp restituisce un risultato al controllo client.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRemoteProgramResult
- Metodo OnRemoteProgramResult Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRemoteProgramResult
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120194"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a><span data-ttu-id="7e745-106">Metodo IMsTscAxEvents:: OnRemoteProgramResult</span><span class="sxs-lookup"><span data-stu-id="7e745-106">IMsTscAxEvents::OnRemoteProgramResult method</span></span>

<span data-ttu-id="7e745-107">Chiamato quando un programma RemoteApp restituisce un risultato al controllo client.</span><span class="sxs-lookup"><span data-stu-id="7e745-107">Called when a RemoteApp program returns a result to the client control.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e745-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e745-108">Syntax</span></span>


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a><span data-ttu-id="7e745-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e745-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e745-110">*bstrRemoteProgram* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e745-110">*bstrRemoteProgram* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e745-111">Nome del programma RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7e745-111">The name of the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="7e745-112">*lError* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e745-112">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e745-113">Risultato del tentativo di avviare il programma RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7e745-113">The result of the attempt to launch the RemoteApp program.</span></span>

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span data-ttu-id="7e745-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="7e745-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7e745-115">Il programma RemoteApp è stato avviato correttamente.</span><span class="sxs-lookup"><span data-stu-id="7e745-115">The RemoteApp program launched successfully.</span></span>

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span data-ttu-id="7e745-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="7e745-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="7e745-117">La sessione remota è bloccata e non è possibile avviare il programma RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7e745-117">The remote session is locked and the RemoteApp program cannot be launched.</span></span> <span data-ttu-id="7e745-118">L'utente deve immettere le proprie credenziali per sbloccare la sessione e quindi avviare il programma RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7e745-118">The user must enter their credentials to unlock the session, and then launch the RemoteApp program.</span></span>

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span data-ttu-id="7e745-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="7e745-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="7e745-120">Il programma RemoteApp ha restituito un errore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="7e745-120">The RemoteApp program returned a protocol error.</span></span>

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span data-ttu-id="7e745-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="7e745-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="7e745-122">Il programma RemoteApp non è presente nell'elenco approvato del server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="7e745-122">The RemoteApp program is not in the approved list of the RD Session Host server.</span></span>

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span data-ttu-id="7e745-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="7e745-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="7e745-124">Il percorso di rete del programma RemoteApp è stato negato.</span><span class="sxs-lookup"><span data-stu-id="7e745-124">The network path to the RemoteApp program was denied.</span></span>

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span data-ttu-id="7e745-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="7e745-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="7e745-126">Il file di programma RemoteApp non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="7e745-126">The RemoteApp program file was not found.</span></span>

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span data-ttu-id="7e745-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="7e745-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="7e745-128">Non è stato possibile avviare il programma RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7e745-128">The RemoteApp program failed to launch.</span></span>

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span data-ttu-id="7e745-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span><span class="sxs-lookup"><span data-stu-id="7e745-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span></span>


</dt> <dd>

<span data-ttu-id="7e745-130">Non è possibile avviare il programma RemoteApp perché la sessione sta attualmente visualizzando il desktop sicuro.</span><span class="sxs-lookup"><span data-stu-id="7e745-130">The RemoteApp program cannot be launched because the session is currently displaying the secure desktop.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7e745-131">*vbIsExecutable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e745-131">*vbIsExecutable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e745-132">Indica se il programma RemoteApp è stato avviato direttamente, usando il nome dell'eseguibile o indirettamente, usando un'associazione di file.</span><span class="sxs-lookup"><span data-stu-id="7e745-132">Indicates whether the RemoteApp program was launched directly, by using the executable name or indirectly, by using a file association.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e745-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e745-133">Return value</span></span>

<span data-ttu-id="7e745-134">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7e745-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e745-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e745-135">Remarks</span></span>

<span data-ttu-id="7e745-136">Implementare questo metodo nel sink di evento per ricevere una notifica che un programma RemoteApp ha restituito un risultato.</span><span class="sxs-lookup"><span data-stu-id="7e745-136">Implement this method in your event sink to receive notification that a RemoteApp program returned a result.</span></span>

<span data-ttu-id="7e745-137">Questo metodo viene chiamato immediatamente dopo che il controllo ActiveX tenta di avviare il programma RemoteApp e il parametro *lError* indica il risultato del tentativo.</span><span class="sxs-lookup"><span data-stu-id="7e745-137">This method is called immediately after the ActiveX control attempts to launch the RemoteApp program, and the *lError* parameter indicates the result of the attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e745-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e745-138">Requirements</span></span>



| <span data-ttu-id="7e745-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e745-139">Requirement</span></span> | <span data-ttu-id="7e745-140">Valore</span><span class="sxs-lookup"><span data-stu-id="7e745-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e745-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e745-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7e745-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7e745-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7e745-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e745-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7e745-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e745-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7e745-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7e745-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="7e745-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e745-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e745-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7e745-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e745-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e745-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e745-149">IID</span><span class="sxs-lookup"><span data-stu-id="7e745-149">IID</span></span><br/>                      | <span data-ttu-id="7e745-150">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="7e745-150">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7e745-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e745-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e745-152">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="7e745-152">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





