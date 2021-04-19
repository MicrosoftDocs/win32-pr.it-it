---
description: Contiene informazioni sul profilo di connessione 802.1 X attualmente utilizzato per l'autenticazione 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Struttura ONEX_CONNECTION_PROFILE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311677"
---
# <a name="onex_connection_profile-structure"></a><span data-ttu-id="581a5-103">Struttura del profilo di \_ connessione Onex \_</span><span class="sxs-lookup"><span data-stu-id="581a5-103">ONEX\_CONNECTION\_PROFILE structure</span></span>

<span data-ttu-id="581a5-104">La struttura del **\_ \_ profilo di connessione Onex** contiene informazioni sul profilo di connessione 802.1 x attualmente utilizzato per l'autenticazione 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-104">The **ONEX\_CONNECTION\_PROFILE** structure contains information on the 802.1X connection profile currently used for 802.1X authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="581a5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="581a5-105">Syntax</span></span>


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a><span data-ttu-id="581a5-106">Members</span><span class="sxs-lookup"><span data-stu-id="581a5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="581a5-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="581a5-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-108">Versione della struttura del **\_ \_ profilo di connessione Onex** .</span><span class="sxs-lookup"><span data-stu-id="581a5-108">The version of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-109">**dwTotalLen**</span><span class="sxs-lookup"><span data-stu-id="581a5-109">**dwTotalLen**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-110">Lunghezza, in byte, della struttura del **\_ \_ profilo di connessione Onex** .</span><span class="sxs-lookup"><span data-stu-id="581a5-110">The length, in bytes, of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-111">**fOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="581a5-111">**fOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-112">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwOneXSupplicantFlags** .</span><span class="sxs-lookup"><span data-stu-id="581a5-112">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwOneXSupplicantFlags** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-113">**fsupplicantMode**</span><span class="sxs-lookup"><span data-stu-id="581a5-113">**fsupplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-114">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **supplicantMode** .</span><span class="sxs-lookup"><span data-stu-id="581a5-114">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **supplicantMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-115">**fauthMode**</span><span class="sxs-lookup"><span data-stu-id="581a5-115">**fauthMode**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-116">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **AuthMode** .</span><span class="sxs-lookup"><span data-stu-id="581a5-116">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **authMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-117">**fHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="581a5-117">**fHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-118">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwHeldPeriod** .</span><span class="sxs-lookup"><span data-stu-id="581a5-118">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwHeldPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-119">**fAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="581a5-119">**fAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-120">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwAuthPeriod** .</span><span class="sxs-lookup"><span data-stu-id="581a5-120">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwAuthPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-121">**fStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="581a5-121">**fStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-122">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwStartPeriod** .</span><span class="sxs-lookup"><span data-stu-id="581a5-122">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwStartPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-123">**fMaxStart**</span><span class="sxs-lookup"><span data-stu-id="581a5-123">**fMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-124">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwMaxStart** .</span><span class="sxs-lookup"><span data-stu-id="581a5-124">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxStart** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-125">**fMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="581a5-125">**fMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-126">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwMaxAuthFailures** .</span><span class="sxs-lookup"><span data-stu-id="581a5-126">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxAuthFailures** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-127">**fNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="581a5-127">**fNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-128">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwNetworkAuthTimeout** .</span><span class="sxs-lookup"><span data-stu-id="581a5-128">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthTimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-129">**fAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="581a5-129">**fAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-130">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **bAllowLogonDialogs** .</span><span class="sxs-lookup"><span data-stu-id="581a5-130">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bAllowLogonDialogs** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-131">**fNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="581a5-131">**fNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-132">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **dwNetworkAuthWithUITimeout** .</span><span class="sxs-lookup"><span data-stu-id="581a5-132">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthWithUITimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-133">**fUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="581a5-133">**fUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-134">Indica se la struttura del **\_ \_ profilo di connessione Onex** contiene dati validi nel membro **bUserBasedVLan** .</span><span class="sxs-lookup"><span data-stu-id="581a5-134">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bUserBasedVLan** member.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-135">**dwOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="581a5-135">**dwOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-136">Set di flag 802.1 X che possono essere presenti nel profilo.</span><span class="sxs-lookup"><span data-stu-id="581a5-136">A set of 802.1X flags that can be present in the profile.</span></span> <span data-ttu-id="581a5-137">Questi flag sono riservati per uso interno da parte del modulo di autenticazione 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="581a5-137">These flags are reserved for internal use by the 802.1X authentication module.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-138">**supplicantMode**</span><span class="sxs-lookup"><span data-stu-id="581a5-138">**supplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-139">Elemento supplicantMode nello schema 802.1 X che specifica il metodo di trasmissione utilizzato per i messaggi di EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="581a5-139">The supplicantMode element in the 802.1X schema that specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="581a5-140">Per ulteriori informazioni, vedere l' [**elemento supplicantMode (Onex)**](onexschema-supplicantmode-onex-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-140">For more information, see the [**supplicantMode (OneX) Element**](onexschema-supplicantmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="581a5-141">Valore</span><span class="sxs-lookup"><span data-stu-id="581a5-141">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="581a5-142">Significato</span><span class="sxs-lookup"><span data-stu-id="581a5-142">Meaning</span></span>                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <span data-ttu-id="581a5-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="581a5-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="581a5-144">EAPOL-Start messaggi non vengono trasmessi.</span><span class="sxs-lookup"><span data-stu-id="581a5-144">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="581a5-145">Valido solo per i profili LAN cablati.</span><span class="sxs-lookup"><span data-stu-id="581a5-145">Valid for wired LAN profiles only.</span></span><br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <span data-ttu-id="581a5-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="581a5-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="581a5-147">Il client determina quando inviare pacchetti di EAPOL-Start in base alla funzionalità di rete.</span><span class="sxs-lookup"><span data-stu-id="581a5-147">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="581a5-148">EAPOL-Start messaggi vengono inviati solo quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="581a5-148">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="581a5-149">Valido solo per i profili LAN cablati.</span><span class="sxs-lookup"><span data-stu-id="581a5-149">Valid for wired LAN profiles only.</span></span><br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <span data-ttu-id="581a5-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="581a5-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="581a5-151">EAPOL-Start messaggi vengono trasmessi come specificato da 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="581a5-151">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="581a5-152">Valido per i profili LAN cablati e wireless.</span><span class="sxs-lookup"><span data-stu-id="581a5-152">Valid for both wired and wireless LAN profiles.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="581a5-153">**authMode**</span><span class="sxs-lookup"><span data-stu-id="581a5-153">**authMode**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-154">Elemento authMode nello schema 802.1 X che specifica il tipo di credenziali utilizzate per l'autenticazione 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="581a5-154">The authMode element in the 802.1X schema that specifies the type of credentials used for 802.1X authentication.</span></span> <span data-ttu-id="581a5-155">Per ulteriori informazioni, vedere l' [**elemento authMode (Onex)**](onexschema-authmode-onex-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-155">For more information, see the [**authMode (OneX) Element**](onexschema-authmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="581a5-156">Valore</span><span class="sxs-lookup"><span data-stu-id="581a5-156">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="581a5-157">Significato</span><span class="sxs-lookup"><span data-stu-id="581a5-157">Meaning</span></span>                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <span data-ttu-id="581a5-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="581a5-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="581a5-159">Usare le credenziali del computer o dell'utente.</span><span class="sxs-lookup"><span data-stu-id="581a5-159">Use machine or user credentials.</span></span> <span data-ttu-id="581a5-160">Quando un utente è connesso, le credenziali dell'utente vengono usate per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="581a5-160">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="581a5-161">Quando nessun utente è connesso, vengono usate le credenziali del computer.</span><span class="sxs-lookup"><span data-stu-id="581a5-161">When no user is logged on, machine credentials are used.</span></span><br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <span data-ttu-id="581a5-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="581a5-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="581a5-163">Usare solo le credenziali del computer.</span><span class="sxs-lookup"><span data-stu-id="581a5-163">Use machine credentials only.</span></span><br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <span data-ttu-id="581a5-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="581a5-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="581a5-165">Usare solo le credenziali utente.</span><span class="sxs-lookup"><span data-stu-id="581a5-165">Use user credentials only.</span></span><br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <span data-ttu-id="581a5-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="581a5-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span></span> </dl>                                 | <span data-ttu-id="581a5-167">Utilizzare solo le credenziali Guest (vuote).</span><span class="sxs-lookup"><span data-stu-id="581a5-167">Use guest (empty) credentials only.</span></span><br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <span data-ttu-id="581a5-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="581a5-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="581a5-169">Non sono state specificate le credenziali da usare.</span><span class="sxs-lookup"><span data-stu-id="581a5-169">Credentials to use are not specified.</span></span><br/>                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="581a5-170">**dwHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="581a5-170">**dwHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-171">Elemento heldPeriod nello schema 802.1 X che specifica il periodo di tempo, in secondi, in cui un client non tenterà di nuovo l'autenticazione dopo un tentativo di autenticazione non riuscito.</span><span class="sxs-lookup"><span data-stu-id="581a5-171">The heldPeriod element in the 802.1X schema that specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span> <span data-ttu-id="581a5-172">Per ulteriori informazioni, vedere l' [**elemento heldPeriod (Onex)**](onexschema-heldperiod-onex-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-172">For more information, see the [**heldPeriod (OneX) Element**](onexschema-heldperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-173">**dwAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="581a5-173">**dwAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-174">Elemento authPeriod nello schema 802.1 X che specifica il periodo di tempo massimo, in secondi, in cui un client attende una risposta dall'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="581a5-174">The authPeriod element in the 802.1X schema that specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="581a5-175">Se non viene ricevuta una risposta entro il periodo specificato, il client presuppone che non sia presente alcun autenticatore nella rete.</span><span class="sxs-lookup"><span data-stu-id="581a5-175">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="581a5-176">Per ulteriori informazioni, vedere l' [**elemento authPeriod (Onex)**](onexschema-authperiod-onex-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-176">For more information, see the [**authPeriod (OneX) Element**](onexschema-authperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-177">**dwStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="581a5-177">**dwStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-178">Elemento startPeriod nello schema 802.1 X che specifica il periodo di tempo, in secondi, di attesa prima dell'invio di un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="581a5-178">The startPeriod element in the 802.1X schema that specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="581a5-179">Viene inviato un messaggio di EAPOL-Start per avviare il processo di autenticazione 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="581a5-179">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span> <span data-ttu-id="581a5-180">Per ulteriori informazioni, vedere l' [**elemento startPeriod (Onex)**](onexschema-startperiod-onex-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-180">For more information, see the [**startPeriod (OneX) Element**](onexschema-startperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-181">**dwMaxStart**</span><span class="sxs-lookup"><span data-stu-id="581a5-181">**dwMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-182">Elemento maxStart nello schema 802.1 X che specifica il numero massimo di messaggi di EAPOL-Start inviati.</span><span class="sxs-lookup"><span data-stu-id="581a5-182">The maxStart element in the 802.1X schema that specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="581a5-183">Una volta inviato il numero massimo di EAPOL-Start messaggi, il client presuppone che non sia presente alcun autenticatore nella rete.</span><span class="sxs-lookup"><span data-stu-id="581a5-183">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="581a5-184">Per ulteriori informazioni, vedere l' [**elemento maxStart (Onex)**](onexschema-maxstart-onex-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-184">For more information, see the [**maxStart (OneX) Element**](onexschema-maxstart-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-185">**dwMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="581a5-185">**dwMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-186">Elemento maxAuthFailures nello schema 802.1 X che specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali.</span><span class="sxs-lookup"><span data-stu-id="581a5-186">The maxAuthFailures element in the 802.1X schema that specifies the maximum number of authentication failures allowed for a set of credentials.</span></span> <span data-ttu-id="581a5-187">Per ulteriori informazioni, vedere l'elemento [**maxAuthFailures (Onex)**](onexschema-maxauthfailures-onex-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-187">For more information, see the [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-188">**dwNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="581a5-188">**dwNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-189">Tempo di attesa, in secondi, per il completamento dell'autenticazione 802.1 X prima di procedere con l'accesso normale.</span><span class="sxs-lookup"><span data-stu-id="581a5-189">The time, in seconds, to wait for 802.1X authentication completion before normal logon proceeds.</span></span> <span data-ttu-id="581a5-190">Questo valore viene utilizzato in scenari Single Sign-on (SSO).</span><span class="sxs-lookup"><span data-stu-id="581a5-190">This value is used in single signon (SSO) scenarios.</span></span> <span data-ttu-id="581a5-191">Il valore predefinito è 10 secondi in un profilo 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="581a5-191">This value defaults to 10 seconds in an 802.1X profile.</span></span> <span data-ttu-id="581a5-192">Per ulteriori informazioni, vedere l' [**elemento maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-192">For more information, see the [**maxDelay (singleSignOn) Element**](onexschema-maxdelay-singlesignon-element.md) in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-193">**dwNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="581a5-193">**dwNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-194">Tempo massimo di attesa, in secondi, per la connessione, nel caso in cui venga visualizzata una finestra di dialogo dell'interfaccia utente che richiede l'input dell'utente durante l'accesso SSO per accesso.</span><span class="sxs-lookup"><span data-stu-id="581a5-194">The maximum duration time, in seconds, to wait for a connection in case a user interface dialog box that requires user input is displayed during the per-logon SSO.</span></span>

<span data-ttu-id="581a5-195">In Windows Vista con SP1 e versioni successive questo valore è hardcoded a 10 minuti e non è configurabile.</span><span class="sxs-lookup"><span data-stu-id="581a5-195">On Windows Vista with SP1 and later, this value is hardcoded to 10 minutes and is not configurable.</span></span> <span data-ttu-id="581a5-196">In Windows Vista Release to Manufacturing, questo valore viene impostato su 60 secondi in un profilo 802.1 X e controllato dall'elemento **maxDelayWithAdditionalDialogs** nello schema.</span><span class="sxs-lookup"><span data-stu-id="581a5-196">On Windows Vista Release to Manufacturing, this value defaults to 60 seconds in an 802.1X profile and was controlled by the **maxDelayWithAdditionalDialogs** element in the schema.</span></span>

<span data-ttu-id="581a5-197">In Windows Vista con SP1 e versioni successive, l'elemento **maxDelayWithAdditionalDialogs** nello schema 802.1 x viene ignorato e deprecato.</span><span class="sxs-lookup"><span data-stu-id="581a5-197">On Windows Vista with SP1 and later, the **maxDelayWithAdditionalDialogs** element in the 802.1X schema is ignored and deprecated.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-198">**bAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="581a5-198">**bAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-199">Valore che specifica se consentire la visualizzazione di finestre di dialogo EAP quando si utilizza SSO di pre-accesso.</span><span class="sxs-lookup"><span data-stu-id="581a5-199">A value that specifies whether to allow EAP dialogs to be displayed when using pre-logon SSO.</span></span> <span data-ttu-id="581a5-200">Per ulteriori informazioni, vedere l'elemento **allowAdditionalDialogs** nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-200">For more information, see the **allowAdditionalDialogs** element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="581a5-201">**bUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="581a5-201">**bUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="581a5-202">Elemento userBasedVirtualLan nello schema 802.1 X che specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="581a5-202">The userBasedVirtualLan element in the 802.1X schema that specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="581a5-203">Alcuni dispositivi NAS (Network Access Server) modificano la VLAN dopo l'autenticazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="581a5-203">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="581a5-204">Quando userBasedVirtualLan è TRUE, il NAS può modificare la VLAN di un dispositivo dopo l'autenticazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="581a5-204">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span> <span data-ttu-id="581a5-205">Per ulteriori informazioni, vedere l' [**elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) nello schema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-205">For more information, see the [**userBasedVirtualLan (singleSignOn) Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) in the 802.1X scheme.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="581a5-206">Commenti</span><span class="sxs-lookup"><span data-stu-id="581a5-206">Remarks</span></span>

<span data-ttu-id="581a5-207">La struttura del **\_ \_ profilo di connessione Onex** viene utilizzata dal modulo 802.1 x, un nuovo componente di configurazione wireless supportato in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="581a5-207">The **ONEX\_CONNECTION\_PROFILE** structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and later.</span></span>

<span data-ttu-id="581a5-208">I [**\_ dati dell' \_ aggiornamento \_ dei risultati di Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contengono informazioni su una modifica dello stato dell'autenticazione 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-208">The [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contains information on a status change to 802.1X authentication.</span></span> <span data-ttu-id="581a5-209">La **struttura \_ \_ \_ dei dati di aggiornamento dei risultati di Onex** viene restituita quando il membro **NotificationSource** della struttura dei [**\_ \_ dati di notifica**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) WLAN è l'origine di **\_ notifica WLAN \_ \_ Onex** e il membro **NotificationCode** della struttura **\_ \_ dei dati di notifica WLAN** per la notifica ricevuta è **OneXNotificationTypeResultUpdate**.</span><span class="sxs-lookup"><span data-stu-id="581a5-209">The **ONEX\_RESULT\_UPDATE\_DATA** structure is returned when the **NotificationSource** member of the [**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) structure is **WLAN\_NOTIFICATION\_SOURCE\_ONEX** and the **NotificationCode** member of the **WLAN\_NOTIFICATION\_DATA** structure for received notification is **OneXNotificationTypeResultUpdate**.</span></span> <span data-ttu-id="581a5-210">Per questa notifica, il membro **pData** della struttura **di \_ \_ dati di notifica WLAN** punta a una struttura di dati di **\_ \_ aggiornamento \_ dei risultati di Onex** che contiene informazioni sulla modifica dello stato di autenticazione 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="581a5-210">For this notification, the **pData** member of the **WLAN\_NOTIFICATION\_DATA** structure points to an **ONEX\_RESULT\_UPDATE\_DATA** structure that contains information on the 802.1X authentication status change.</span></span>

<span data-ttu-id="581a5-211">Se il membro **fOneXAuthParams** nella struttura [**\_ \_ \_ dei dati di aggiornamento dei risultati di Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) è impostato, il membro **authParams** della struttura **\_ \_ \_ dei dati di aggiornamento dei risultati Onex** contiene una struttura di [**\_ \_ BLOB di variabili Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) con una struttura di [**\_ \_ parametri auth Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) incorporata a partire dal membro **dwOffset** del **\_ \_ BLOB della variabile Onex**.</span><span class="sxs-lookup"><span data-stu-id="581a5-211">If the **fOneXAuthParams** member in the [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) structure is set, then the **authParams** member of the **ONEX\_RESULT\_UPDATE\_DATA** structure contains an [**ONEX\_VARIABLE\_BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) structure with an [**ONEX\_AUTH\_PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span> <span data-ttu-id="581a5-212">Il membro **oneXConnProfile** della struttura **Onex \_ auth \_ params** contiene una struttura **\_ \_ BLOB della variabile Onex** con una struttura del **\_ \_ profilo di connessione Onex** incorporata a partire dal membro **dwOffset** del **\_ \_ BLOB della variabile Onex**.</span><span class="sxs-lookup"><span data-stu-id="581a5-212">The **oneXConnProfile** member of the **ONEX\_AUTH\_PARAMS** structure contains an **ONEX\_VARIABLE\_BLOB** structure with an **ONEX\_CONNECTION\_PROFILE** structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span>

<span data-ttu-id="581a5-213">La struttura del **\_ \_ profilo di connessione Onex** non è definita in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="581a5-213">The **ONEX\_CONNECTION\_PROFILE** structure is not defined in a public header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="581a5-214">Requisiti</span><span class="sxs-lookup"><span data-stu-id="581a5-214">Requirements</span></span>



| <span data-ttu-id="581a5-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="581a5-215">Requirement</span></span> | <span data-ttu-id="581a5-216">Valore</span><span class="sxs-lookup"><span data-stu-id="581a5-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="581a5-217">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="581a5-217">Minimum supported client</span></span><br/> | <span data-ttu-id="581a5-218">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="581a5-218">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="581a5-219">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="581a5-219">Minimum supported server</span></span><br/> | <span data-ttu-id="581a5-220">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="581a5-220">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="581a5-221">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="581a5-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581a5-222">Informazioni sull'architettura di ACM</span><span class="sxs-lookup"><span data-stu-id="581a5-222">About the ACM Architecture</span></span>](about-the-acm-architecture.md)
</dt> <dt>

[<span data-ttu-id="581a5-223">Schema OneX</span><span class="sxs-lookup"><span data-stu-id="581a5-223">OneX Schema</span></span>](onexschema-schema.md)
</dt> <dt>

[<span data-ttu-id="581a5-224">**Elemento authMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="581a5-224">**authMode (OneX) Element**</span></span>](onexschema-authmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-225">**Elemento authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="581a5-225">**authPeriod (OneX) Element**</span></span>](onexschema-authperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-226">**Elemento heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="581a5-226">**heldPeriod (OneX) Element**</span></span>](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-227">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="581a5-227">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-228">**Elemento maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="581a5-228">**maxStart (OneX) Element**</span></span>](onexschema-maxstart-onex-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-229">**Elemento startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="581a5-229">**startPeriod (OneX) Element**</span></span>](onexschema-startperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-230">**Elemento supplicantMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="581a5-230">**supplicantMode (OneX) Element**</span></span>](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-231">**Elemento userBasedVirtualLan (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="581a5-231">**userBasedVirtualLan (singleSignOn) Element**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-232">**\_parametri di autenticazione Onex \_**</span><span class="sxs-lookup"><span data-stu-id="581a5-232">**ONEX\_AUTH\_PARAMS**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[<span data-ttu-id="581a5-233">**\_tipo di notifica Onex \_**</span><span class="sxs-lookup"><span data-stu-id="581a5-233">**ONEX\_NOTIFICATION\_TYPE**</span></span>](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[<span data-ttu-id="581a5-234">**\_ \_ dati aggiornamento risultati \_ Onex**</span><span class="sxs-lookup"><span data-stu-id="581a5-234">**ONEX\_RESULT\_UPDATE\_DATA**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[<span data-ttu-id="581a5-235">**Elemento dello schema OneX**</span><span class="sxs-lookup"><span data-stu-id="581a5-235">**OneX Schema Element**</span></span>](onexschema-onex-element.md)
</dt> <dt>

[<span data-ttu-id="581a5-236">**\_BLOB variabile \_ Onex**</span><span class="sxs-lookup"><span data-stu-id="581a5-236">**ONEX\_VARIABLE\_BLOB**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

<span data-ttu-id="581a5-237">[**\_dati di notifica WLAN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="581a5-237">[**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="581a5-238">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="581a5-238">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
