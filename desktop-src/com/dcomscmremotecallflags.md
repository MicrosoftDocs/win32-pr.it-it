---
title: DCOMSCMRemoteCallFlags
description: Controlla il comportamento delle chiamate da Gestione controllo servizi DCOM locale (DCOMSCM) a una DCOMSCM remota.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valore DCOMSCMRemoteCallFlags del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047416"
---
# <a name="dcomscmremotecallflags"></a><span data-ttu-id="acda9-104">DCOMSCMRemoteCallFlags</span><span class="sxs-lookup"><span data-stu-id="acda9-104">DCOMSCMRemoteCallFlags</span></span>

<span data-ttu-id="acda9-105">Controlla il comportamento delle chiamate da Gestione controllo servizi DCOM locale (DCOMSCM) a una DCOMSCM remota.</span><span class="sxs-lookup"><span data-stu-id="acda9-105">Controls the behavior of calls from the local DCOM Service Control Manager (DCOMSCM) to a remote DCOMSCM.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="acda9-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="acda9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a><span data-ttu-id="acda9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="acda9-107">Remarks</span></span>

<span data-ttu-id="acda9-108">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="acda9-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="acda9-109">Valore</span><span class="sxs-lookup"><span data-stu-id="acda9-109">Value</span></span> | <span data-ttu-id="acda9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acda9-110">Description</span></span>                                       |
|-------|---------------------------------------------------|
| <span data-ttu-id="acda9-111">0x1</span><span class="sxs-lookup"><span data-stu-id="acda9-111">0x1</span></span>   | <span data-ttu-id="acda9-112">**DCOMSCM \_ Activation \_ use \_ All \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="acda9-112">**DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES**</span></span>  |
| <span data-ttu-id="acda9-113">0x2</span><span class="sxs-lookup"><span data-stu-id="acda9-113">0x2</span></span>   | <span data-ttu-id="acda9-114">**attivazione di DCOMSCM non \_ \_ consente la \_ chiamata non protetta \_**</span><span class="sxs-lookup"><span data-stu-id="acda9-114">**DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL**</span></span> |
| <span data-ttu-id="acda9-115">0x4</span><span class="sxs-lookup"><span data-stu-id="acda9-115">0x4</span></span>   | <span data-ttu-id="acda9-116">**DCOMSCM \_ Risolvi \_ use \_ All \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="acda9-116">**DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES**</span></span>     |
| <span data-ttu-id="acda9-117">0x8</span><span class="sxs-lookup"><span data-stu-id="acda9-117">0x8</span></span>   | <span data-ttu-id="acda9-118">**DCOMSCM \_ risolvere non \_ consentire una \_ chiamata non sicura \_**</span><span class="sxs-lookup"><span data-stu-id="acda9-118">**DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL**</span></span>    |
| <span data-ttu-id="acda9-119">0x10</span><span class="sxs-lookup"><span data-stu-id="acda9-119">0x10</span></span>  | <span data-ttu-id="acda9-120">**DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE**</span><span class="sxs-lookup"><span data-stu-id="acda9-120">**DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE**</span></span>         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a><span data-ttu-id="acda9-121">DCOMSCM \_ Activation \_ use \_ All \_ AUTHNSERVICES Description</span><span class="sxs-lookup"><span data-stu-id="acda9-121">DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="acda9-122">Quando il client invia una richiesta di attivazione che usa le impostazioni di sicurezza predefinite, il DCOMSCM locale usa il servizio di autenticazione Negotiate quando effettua la chiamata RPC di attivazione al DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="acda9-122">When the client issues an activation request that uses the default security settings, the local DCOMSCM uses the Negotiate authentication service when making the activation RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="acda9-123">Se la chiamata ha esito negativo, il DCOMSCM locale rende la chiamata RPC di attivazione con nessuna sicurezza.</span><span class="sxs-lookup"><span data-stu-id="acda9-123">If the call fails, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="acda9-124">**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC di attivazione che utilizza il servizio di autenticazione Negotiate ha esito negativo, il DCOMSCM locale effettua la chiamata RPC di attivazione utilizzando Kerberos, NTLM o altri provider di sicurezza configurati.</span><span class="sxs-lookup"><span data-stu-id="acda9-124">**Windows Server 2003 and Windows XP/2000:** If the activation RPC call that uses the Negotiate authentication service fails, the local DCOMSCM makes the activation RPC call using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="acda9-125">Se non funziona alcun provider di sicurezza, il DCOMSCM locale effettua la chiamata RPC di attivazione senza alcuna sicurezza.</span><span class="sxs-lookup"><span data-stu-id="acda9-125">If no security providers work, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="acda9-126">Impostando questo flag, è possibile eseguire il DCOMSCM locale in Windows Vista o versione successiva per comportarsi come i sistemi precedenti a vista.</span><span class="sxs-lookup"><span data-stu-id="acda9-126">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="acda9-127">Non è consigliabile impostare questo flag a meno che non sia necessario per motivi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="acda9-127">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a><span data-ttu-id="acda9-128">DCOMSCM \_ Activation non \_ consente la descrizione della \_ chiamata non protetta \_</span><span class="sxs-lookup"><span data-stu-id="acda9-128">DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="acda9-129">Se l'attivazione di Dcomscm non consente l'impostazione del flag di **\_ \_ \_ \_ chiamata non sicuro** , il Dcomscm locale non esegue una chiamata RPC di attivazione non protetta.</span><span class="sxs-lookup"><span data-stu-id="acda9-129">If the **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure activation RPC call.</span></span> <span data-ttu-id="acda9-130">Per consentire ai client di effettuare richieste di attivazione con impostazioni di sicurezza non predefinite, specificare la struttura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) quando si esegue la richiesta di attivazione.</span><span class="sxs-lookup"><span data-stu-id="acda9-130">To enable clients to make activation requests with non-default security settings, specify the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure when making the activation request.</span></span> <span data-ttu-id="acda9-131">In questo caso, l' **attivazione di Dcomscm \_ \_ utilizza \_ tutti i \_** flag di chiamata AUTHNSERVICES e Dcomscm che non consentono l'attivazione dei flag di **\_ \_ \_ \_ chiamata non protetti** .</span><span class="sxs-lookup"><span data-stu-id="acda9-131">In this case, the **DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES** and **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flags are ignored.</span></span>

<span data-ttu-id="acda9-132">Non è consigliabile impostare questo flag a meno che tutti i client e i server nella rete non siano completamente autenticati.</span><span class="sxs-lookup"><span data-stu-id="acda9-132">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_resolve_use_all_authnservices-description"></a><span data-ttu-id="acda9-133">DCOMSCM \_ Risolvi \_ use \_ All \_ AUTHNSERVICES Description</span><span class="sxs-lookup"><span data-stu-id="acda9-133">DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="acda9-134">Quando il client esegue l'unmarshalling di un riferimento a un oggetto, il DCOMSCM locale usa il servizio di autenticazione Negotiate durante la chiamata RPC di risoluzione OXID al DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="acda9-134">When the client unmarshals an object reference, the local DCOMSCM uses the Negotiate authentication service when making the OXID Resolution RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="acda9-135">Se la chiamata ha esito negativo, il DCOMSCM locale fa in modo che la chiamata RPC di risoluzione OXID non usi alcuna sicurezza.</span><span class="sxs-lookup"><span data-stu-id="acda9-135">If the call fails, the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="acda9-136">**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC di risoluzione OXID che usa il servizio di autenticazione Negotiate ha esito negativo, il DCOMSCM locale esegue la chiamata RPC di risoluzione OXID usando Kerberos, NTLM o altri provider di sicurezza configurati.</span><span class="sxs-lookup"><span data-stu-id="acda9-136">**Windows Server 2003 and Windows XP/2000:** If the OXID Resolution RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the OXID Resolution RPC call by using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="acda9-137">Se non funziona alcun provider di sicurezza, il DCOMSCM locale esegue la chiamata RPC di risoluzione OXID senza alcuna sicurezza.</span><span class="sxs-lookup"><span data-stu-id="acda9-137">If no security providers work, then the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="acda9-138">Impostando questo flag, è possibile eseguire il DCOMSCM locale in Windows Vista o versione successiva per comportarsi come i sistemi precedenti a vista.</span><span class="sxs-lookup"><span data-stu-id="acda9-138">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="acda9-139">Non è consigliabile impostare questo flag a meno che non sia necessario per motivi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="acda9-139">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a><span data-ttu-id="acda9-140">DCOMSCM \_ risolvere non \_ consentire la descrizione della \_ chiamata non protetta \_</span><span class="sxs-lookup"><span data-stu-id="acda9-140">DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="acda9-141">Se è impostata l'opzione **Dcomscm \_ Resolve \_ unallow \_ unsecure \_ Call** flag, il Dcomscm locale non esegue una chiamata RPC di risoluzione OXID non protetta.</span><span class="sxs-lookup"><span data-stu-id="acda9-141">If the **DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure OXID Resolution RPC call.</span></span> <span data-ttu-id="acda9-142">Inoltre, il DCOMSCM locale non esegue una chiamata RPC ping Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="acda9-142">In addition, the local DCOMSCM does not make an unsecure garbage collection Ping RPC call.</span></span> <span data-ttu-id="acda9-143">Non è consigliabile impostare questo flag a meno che tutti i client e i server nella rete non siano completamente autenticati.</span><span class="sxs-lookup"><span data-stu-id="acda9-143">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_ping_use_mid_authnservice-description"></a><span data-ttu-id="acda9-144">DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE Description</span><span class="sxs-lookup"><span data-stu-id="acda9-144">DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE Description</span></span>

<span data-ttu-id="acda9-145">Il DCOMSCM locale usa il servizio di autenticazione Negotiate quando effettua la chiamata RPC ping della Garbage Collection al DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="acda9-145">The local DCOMSCM uses the Negotiate authentication service when making the garbage-collection Ping RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="acda9-146">Se la chiamata ha esito negativo, il DCOMSCM locale rende la chiamata RPC ping della Garbage Collection che non usa alcuna sicurezza.</span><span class="sxs-lookup"><span data-stu-id="acda9-146">If the call fails, the local DCOMSCM makes the garbage-collection Ping RPC call using no security.</span></span>

<span data-ttu-id="acda9-147">**Windows Server 2003 e Windows XP/2000:** Se la chiamata RPC ping della Garbage Collection con il servizio di autenticazione Negotiate ha esito negativo, il DCOMSCM locale rende la chiamata RPC ping Garbage Collection tramite Kerberos, NTLM e altri provider di sicurezza configurati.</span><span class="sxs-lookup"><span data-stu-id="acda9-147">**Windows Server 2003 and Windows XP/2000:** If the garbage-collection Ping RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the garbage collection Ping RPC call by using Kerberos, NTLM, and other configured security providers.</span></span> <span data-ttu-id="acda9-148">Se non è disponibile alcun provider di sicurezza, il DCOMSCM locale rende la chiamata RPC ping Garbage Collection usando nessuna sicurezza.</span><span class="sxs-lookup"><span data-stu-id="acda9-148">If no security providers work, then the local DCOMSCM makes the garbage collection Ping RPC call using no security.</span></span>

<span data-ttu-id="acda9-149">Impostando questo flag, è possibile eseguire il DCOMSCM locale in Windows Vista o versione successiva per comportarsi come i sistemi precedenti a vista.</span><span class="sxs-lookup"><span data-stu-id="acda9-149">By setting this flag, the local DCOMSCM on Windows Vista or above can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="acda9-150">Non è consigliabile impostare **Dcomscm \_ ping \_ use \_ Mid \_ AUTHNSERVICE** flag, a meno che non sia necessario per motivi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="acda9-150">It is not recommended to set the **DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE** flag unless required for compatibility reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acda9-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acda9-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acda9-152">Autenticazione per le connessioni remote</span><span class="sxs-lookup"><span data-stu-id="acda9-152">Authentication for Remote Connections</span></span>](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[<span data-ttu-id="acda9-153">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="acda9-153">EnableDCOM</span></span>](enabledcom.md)
</dt> <dt>

[<span data-ttu-id="acda9-154">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="acda9-154">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="acda9-155">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="acda9-155">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 