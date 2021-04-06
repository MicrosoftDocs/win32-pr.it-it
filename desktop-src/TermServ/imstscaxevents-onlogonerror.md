---
title: Metodo IMsTscAxEvents OnLogonError
description: Chiamato quando si verifica un errore di accesso o un altro evento di accesso.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnLogonError
- Metodo OnLogonError Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnLogonError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742119"
---
# <a name="imstscaxeventsonlogonerror-method"></a><span data-ttu-id="5fd4b-106">Metodo IMsTscAxEvents:: OnLogonError</span><span class="sxs-lookup"><span data-stu-id="5fd4b-106">IMsTscAxEvents::OnLogonError method</span></span>

<span data-ttu-id="5fd4b-107">Chiamato quando si verifica un errore di accesso o un altro evento di accesso.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-107">Called when a logon error or other logon event occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd4b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fd4b-108">Syntax</span></span>


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a><span data-ttu-id="5fd4b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fd4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd4b-110">*lError* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5fd4b-110">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd4b-111">Codice di errore di accesso.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-111">The logon error code.</span></span> <span data-ttu-id="5fd4b-112">Questo elenco di codici non è esaustivo.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-112">This list of codes is not exhaustive.</span></span>

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span data-ttu-id="5fd4b-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Arbitraggio \_ \_ \_ Opzioni di Bump del codice** (-5 (0xFFFFFFFB))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**ARBITRATION\_CODE\_BUMP\_OPTIONS** (-5 (0xFFFFFFFB))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-114">Winlogon Visualizza la finestra di dialogo **contesa di sessione** .</span><span class="sxs-lookup"><span data-stu-id="5fd4b-114">Winlogon is displaying the **Session Contention** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span data-ttu-id="5fd4b-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Arbitraggio \_ \_ \_ Accesso continuo al codice** (-2 (0xfffffffe))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**ARBITRATION\_CODE\_CONTINUE\_LOGON** (-2 (0xFFFFFFFE))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-116">Winlogon continua con il processo di accesso.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-116">Winlogon is continuing with the logon process.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span data-ttu-id="5fd4b-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Arbitraggio \_ \_ \_ Terminazione continua del codice** (-3 (0xFFFFFFFD))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**ARBITRATION\_CODE\_CONTINUE\_TERMINATE** (-3 (0xFFFFFFFD))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-118">Winlogon termina in modo invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-118">Winlogon is ending silently.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span data-ttu-id="5fd4b-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Arbitraggio \_ \_ \_ Finestra di dialogo codice noperm** (-6 (0xFFFFFFFA))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**ARBITRATION\_CODE\_NOPERM\_DIALOG** (-6 (0xFFFFFFFA))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-120">Winlogon Visualizza la finestra di dialogo **Nessuna autorizzazione** .</span><span class="sxs-lookup"><span data-stu-id="5fd4b-120">Winlogon is displaying the **No Permissions** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span data-ttu-id="5fd4b-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Arbitraggio \_ \_Finestra di \_ dialogo del codice rifiutato** (-7 (0xFFFFFFF9))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**ARBITRATION\_CODE\_REFUSED\_DIALOG** (-7 (0xFFFFFFF9))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-122">Winlogon Visualizza la finestra di dialogo **Disconnetti rifiutato** .</span><span class="sxs-lookup"><span data-stu-id="5fd4b-122">Winlogon is displaying the **Disconnect Refused** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span data-ttu-id="5fd4b-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Arbitraggio \_ \_ \_ Opzioni di ricognizione del codice** (-4 (0xFFFFFFFC))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**ARBITRATION\_CODE\_RECONN\_OPTIONS** (-4 (0xFFFFFFFC))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-124">Winlogon Visualizza la finestra di dialogo **Riconnetti** .</span><span class="sxs-lookup"><span data-stu-id="5fd4b-124">Winlogon is displaying the **Reconnect** dialog box.</span></span>

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span data-ttu-id="5fd4b-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Errore \_ \_Accesso al codice \_ negato** (-1 (0xFFFFFFFF))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**ERROR\_CODE\_ACCESS\_DENIED** (-1 (0xFFFFFFFF))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-126">All'utente è stato negato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-126">The user was denied access.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span data-ttu-id="5fd4b-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Accesso \_ \_ \_ Password errata non riuscita** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**LOGON\_FAILED\_BAD\_PASSWORD** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-128">Accesso non riuscito perché le credenziali di accesso non sono valide.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-128">The logon failed because the logon credentials are not valid.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span data-ttu-id="5fd4b-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Accesso \_ ERRORE \_ altro** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**LOGON\_FAILED\_OTHER** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-130">Si è verificato un altro errore di accesso o post-accesso.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-130">Another logon or post-logon error occurred.</span></span> <span data-ttu-id="5fd4b-131">Il client Desktop remoto Visualizza una schermata di accesso all'utente.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-131">The Remote Desktop client displays a logon screen to the user.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span data-ttu-id="5fd4b-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Accesso \_ \_ \_ Password di aggiornamento non riuscita** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**LOGON\_FAILED\_UPDATE\_PASSWORD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-133">La password è scaduta.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-133">The password is expired.</span></span> <span data-ttu-id="5fd4b-134">Per continuare l'accesso, l'utente deve aggiornare la password.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-134">The user must update their password to continue logging on.</span></span>

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span data-ttu-id="5fd4b-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Accesso \_ AVVISO** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**LOGON\_WARNING** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-136">Il client Desktop remoto Visualizza una finestra di dialogo che contiene informazioni importanti per l'utente.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-136">The Remote Desktop client displays a dialog box that contains important information for the user.</span></span>

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span data-ttu-id="5fd4b-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Stato \_ di \_Restrizione account** (-1073741714 (0xC000006E))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**STATUS\_ACCOUNT\_RESTRICTION** (-1073741714 (0xC000006E))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-138">Il nome utente e le informazioni di autenticazione sono validi, ma l'autenticazione è stata bloccata a causa di restrizioni relative all'account utente, ad esempio restrizioni relative all'ora del giorno.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-138">The user name and authentication information are valid, but authentication was blocked due to restrictions on the user account, such as time-of-day restrictions.</span></span>

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span data-ttu-id="5fd4b-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Stato \_ di \_Errore di accesso** (-1073741715 (0xc000006d))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**STATUS\_LOGON\_FAILURE** (-1073741715 (0xC000006D))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-140">Il tentativo di accesso non è valido.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-140">The attempted logon is not valid.</span></span> <span data-ttu-id="5fd4b-141">Ciò è dovuto a un nome utente errato o a informazioni di autenticazione non corrette.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-141">This is due to either an incorrect user name or incorrect authentication information.</span></span>

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span data-ttu-id="5fd4b-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Stato \_ di La PASSWORD \_ deve essere \_ modificata** (-1073741276 (0xC0000224))</span><span class="sxs-lookup"><span data-stu-id="5fd4b-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**STATUS\_PASSWORD\_MUST\_CHANGE** (-1073741276 (0xC0000224))</span></span>


</dt> <dd>

<span data-ttu-id="5fd4b-143">La password è scaduta.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-143">The password is expired.</span></span> <span data-ttu-id="5fd4b-144">Per continuare l'accesso, l'utente deve aggiornare la password.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-144">The user must update their password to continue logging on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd4b-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fd4b-145">Return value</span></span>

<span data-ttu-id="5fd4b-146">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd4b-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fd4b-147">Remarks</span></span>

<span data-ttu-id="5fd4b-148">Implementare questo metodo nel sink di evento per ricevere una notifica che si è verificato un errore di accesso.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-148">Implement this method in your event sink to receive notification that a logon error has occurred.</span></span>

<span data-ttu-id="5fd4b-149">Questo elenco di codici non è esaustivo.</span><span class="sxs-lookup"><span data-stu-id="5fd4b-149">This list of codes is not exhaustive.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd4b-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fd4b-150">Requirements</span></span>



| <span data-ttu-id="5fd4b-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd4b-151">Requirement</span></span> | <span data-ttu-id="5fd4b-152">Valore</span><span class="sxs-lookup"><span data-stu-id="5fd4b-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd4b-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fd4b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd4b-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fd4b-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5fd4b-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fd4b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd4b-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fd4b-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5fd4b-157">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5fd4b-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="5fd4b-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fd4b-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5fd4b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="5fd4b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fd4b-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fd4b-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5fd4b-161">IID</span><span class="sxs-lookup"><span data-stu-id="5fd4b-161">IID</span></span><br/>                      | <span data-ttu-id="5fd4b-162">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="5fd4b-162">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5fd4b-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fd4b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd4b-164">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="5fd4b-164">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





