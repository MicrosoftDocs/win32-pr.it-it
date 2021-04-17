---
description: Concede lo stato attendibile della condivisione DDE specificato all'interno del contesto degli utenti corrente.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Funzione NDdeSetTrustedShare (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524954"
---
# <a name="nddesettrustedshare-function"></a><span data-ttu-id="0a42c-103">NDdeSetTrustedShare (funzione)</span><span class="sxs-lookup"><span data-stu-id="0a42c-103">NDdeSetTrustedShare function</span></span>

<span data-ttu-id="0a42c-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="0a42c-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="0a42c-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="0a42c-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="0a42c-106">Concede lo stato attendibile della condivisione DDE specificato all'interno del contesto dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="0a42c-106">Grants the specified DDE share trusted status within the current user's context.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a42c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a42c-107">Syntax</span></span>


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a><span data-ttu-id="0a42c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a42c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a42c-109">*lpszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a42c-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a42c-110">Nome del server di cui è necessario modificare il DSDM.</span><span class="sxs-lookup"><span data-stu-id="0a42c-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="0a42c-111">*lpszShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a42c-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a42c-112">Nome della condivisione a cui concedere lo stato attendibile.</span><span class="sxs-lookup"><span data-stu-id="0a42c-112">The name of the share to be granted trusted status.</span></span> <span data-ttu-id="0a42c-113">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0a42c-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0a42c-114">*dwTrustOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a42c-114">*dwTrustOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a42c-115">Opzioni che interessano lo stato attendibile della condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="0a42c-115">The options affecting the trusted status of the DDE share.</span></span> <span data-ttu-id="0a42c-116">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a42c-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0a42c-117">Opzione</span><span class="sxs-lookup"><span data-stu-id="0a42c-117">Option</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="0a42c-118">Significato</span><span class="sxs-lookup"><span data-stu-id="0a42c-118">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="0a42c-119"><dt>**NDDE \_ CMD \_ Mostra \_ maschera**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="0a42c-119"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="0a42c-120">Maschera utilizzata per ottenere il valore utilizzato per eseguire l'override dello stato di visualizzazione della condivisione DDE, se \_ \_ è impostato NDDE Trust cmd \_ show.</span><span class="sxs-lookup"><span data-stu-id="0a42c-120">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="0a42c-121"><dt>**NDDE \_ TRUST \_ cmd \_ Mostra**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="0a42c-121"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="0a42c-122">Eseguire l'override dello stato di visualizzazione specificato nella DSDM della condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="0a42c-122">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="0a42c-123"><dt>**NDDE \_ Condivisione di ATTENDIBILità \_ \_ del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="0a42c-123"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="0a42c-124">Rimuovere lo stato attendibile della condivisione.</span><span class="sxs-lookup"><span data-stu-id="0a42c-124">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="0a42c-125"><dt>**NDDE \_ 0x40000000L \_ \_ init condivisione attendibile**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0a42c-125"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="0a42c-126">Consentire a un client di avviare l'applicazione se è già in esecuzione nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0a42c-126">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="0a42c-127"><dt>**NDDE \_ 0x80000000L \_ di \_ inizio condivisione attendibilità**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0a42c-127"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="0a42c-128">Consente all'applicazione di essere avviata nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0a42c-128">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a42c-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a42c-129">Return value</span></span>

<span data-ttu-id="0a42c-130">Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="0a42c-130">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="0a42c-131">Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="0a42c-131">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a42c-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a42c-132">Remarks</span></span>

<span data-ttu-id="0a42c-133">È innanzitutto necessario creare la condivisione DDE con [**NDDEShareAdd**](nddeshareadd.md).</span><span class="sxs-lookup"><span data-stu-id="0a42c-133">The DDE share must first be created with [**NDdeShareAdd**](nddeshareadd.md).</span></span>

<span data-ttu-id="0a42c-134">Se viene chiamato **NDdeSetTrustedShare** con *dwTrustOptions* impostato su zero, la condivisione attendibile perderà lo stato attendibile.</span><span class="sxs-lookup"><span data-stu-id="0a42c-134">If **NDdeSetTrustedShare** is called with *dwTrustOptions* set to zero, the trusted share loses its trusted status.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a42c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a42c-135">Requirements</span></span>



| <span data-ttu-id="0a42c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a42c-136">Requirement</span></span> | <span data-ttu-id="0a42c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="0a42c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a42c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a42c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0a42c-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a42c-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0a42c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a42c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0a42c-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a42c-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0a42c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a42c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a42c-143"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a42c-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a42c-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a42c-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a42c-145"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a42c-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0a42c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0a42c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a42c-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a42c-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a42c-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0a42c-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0a42c-149">**NDdeSetTrustedShareW** (Unicode) e **NDdeSetTrustedShareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0a42c-149">**NDdeSetTrustedShareW** (Unicode) and **NDdeSetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="0a42c-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a42c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a42c-151">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="0a42c-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="0a42c-152">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="0a42c-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="0a42c-153">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="0a42c-153">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




