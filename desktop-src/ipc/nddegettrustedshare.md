---
description: Recupera le opzioni associate a una condivisione DDE presente nell'elenco utenti del server di condivisioni attendibili.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Funzione NDdeGetTrustedShare (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305713"
---
# <a name="nddegettrustedshare-function"></a><span data-ttu-id="9dd1c-103">NDdeGetTrustedShare (funzione)</span><span class="sxs-lookup"><span data-stu-id="9dd1c-103">NDdeGetTrustedShare function</span></span>

<span data-ttu-id="9dd1c-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="9dd1c-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="9dd1c-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="9dd1c-106">Recupera le opzioni associate a una condivisione DDE presente nell'elenco di condivisioni attendibili dell'utente del server.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-106">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd1c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9dd1c-107">Syntax</span></span>


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a><span data-ttu-id="9dd1c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9dd1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd1c-109">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dd1c-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd1c-110">Nome del server in cui risiede l'DSDM.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="9dd1c-111">*lpszShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dd1c-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd1c-112">Nome della condivisione di cui viene eseguita la query sullo stato attendibile.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-112">The share name whose trusted status is being queried.</span></span> <span data-ttu-id="9dd1c-113">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9dd1c-114">*lpdwTrustOptions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9dd1c-114">*lpdwTrustOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd1c-115">Puntatore a una variabile che riceve le opzioni di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-115">A pointer to a variable that receives the trust options.</span></span> <span data-ttu-id="9dd1c-116">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-116">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="9dd1c-117">Sono disponibili le seguenti opzioni di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-117">The following trust options are available.</span></span>



| <span data-ttu-id="9dd1c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9dd1c-118">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="9dd1c-119">Significato</span><span class="sxs-lookup"><span data-stu-id="9dd1c-119">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="9dd1c-120"><dt>**NDDE \_ CMD \_ Mostra \_ maschera**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="9dd1c-120"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="9dd1c-121">Maschera utilizzata per ottenere il valore utilizzato per eseguire l'override dello stato di visualizzazione della condivisione DDE, se \_ \_ è impostato NDDE Trust cmd \_ show.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-121">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="9dd1c-122"><dt>**NDDE \_ TRUST \_ cmd \_ Mostra**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="9dd1c-122"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="9dd1c-123">Eseguire l'override dello stato di visualizzazione specificato nella DSDM della condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-123">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="9dd1c-124"><dt>**NDDE \_ Condivisione di ATTENDIBILità \_ \_ del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="9dd1c-124"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="9dd1c-125">Rimuovere lo stato attendibile della condivisione.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-125">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="9dd1c-126"><dt>**NDDE \_ 0x40000000L \_ \_ init condivisione attendibile**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9dd1c-126"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="9dd1c-127">Consentire a un client di avviare l'applicazione se è già in esecuzione nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-127">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="9dd1c-128"><dt>**NDDE \_ 0x80000000L \_ di \_ inizio condivisione attendibilità**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9dd1c-128"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="9dd1c-129">Consente all'applicazione di essere avviata nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-129">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="9dd1c-130">*lpdwShareModId0* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9dd1c-130">*lpdwShareModId0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd1c-131">Puntatore a una variabile che riceve la prima parte dell'identificatore di modifica della condivisione attendibile.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-131">A pointer to a variable that receives the first part of the trusted share modify identifier.</span></span> <span data-ttu-id="9dd1c-132">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-132">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9dd1c-133">*lpdwShareModId1* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9dd1c-133">*lpdwShareModId1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd1c-134">Puntatore a una variabile che riceve la seconda parte dell'identificatore di modifica della condivisione attendibile.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-134">A pointer to a variable that receives the second part of the trusted share modify identifier.</span></span> <span data-ttu-id="9dd1c-135">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-135">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd1c-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9dd1c-136">Return value</span></span>

<span data-ttu-id="9dd1c-137">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-137">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="9dd1c-138">Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="9dd1c-138">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd1c-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dd1c-139">Remarks</span></span>

<span data-ttu-id="9dd1c-140">L'identificatore di modifica della condivisione attendibile riflette la versione della condivisione DDE in DSDM al momento dell'iniziale concessione dello stato attendibile per la condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-140">The trusted share modify identifier reflects the version of the DDE share in the DSDM at the time the DDE share was initially granted trusted status.</span></span> <span data-ttu-id="9dd1c-141">L'identificatore di modifica della condivisione attendibile viene utilizzato principalmente per rimuovere le condivisioni attendibili obsolete.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-141">The trusted share modify identifier is primarily used to remove obsolete trusted shares.</span></span> <span data-ttu-id="9dd1c-142">Tuttavia, l'utente non deve rimuovere le condivisioni attendibili obsolete.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-142">However, the user does not need to remove obsolete trusted shares.</span></span> <span data-ttu-id="9dd1c-143">L'agente DDE di rete rimuove le condivisioni obsolete per conto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9dd1c-143">The network DDE agent removes obsolete shares on the user's behalf.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd1c-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dd1c-144">Requirements</span></span>



| <span data-ttu-id="9dd1c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dd1c-145">Requirement</span></span> | <span data-ttu-id="9dd1c-146">Valore</span><span class="sxs-lookup"><span data-stu-id="9dd1c-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd1c-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dd1c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd1c-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9dd1c-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9dd1c-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dd1c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd1c-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9dd1c-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9dd1c-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dd1c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dd1c-152"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd1c-152"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="9dd1c-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="9dd1c-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="9dd1c-154"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dd1c-154"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9dd1c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="9dd1c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dd1c-156"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dd1c-156"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="9dd1c-157">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9dd1c-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9dd1c-158">**NDdeGetTrustedShareW** (Unicode) e **NDdeGetTrustedShareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9dd1c-158">**NDdeGetTrustedShareW** (Unicode) and **NDdeGetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="9dd1c-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dd1c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd1c-160">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="9dd1c-160">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="9dd1c-161">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="9dd1c-161">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="9dd1c-162">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="9dd1c-162">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

 




