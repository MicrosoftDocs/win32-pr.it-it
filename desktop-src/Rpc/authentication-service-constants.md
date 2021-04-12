---
title: Costanti Authentication-Service (rpcdce. h)
description: Le costanti del servizio di autenticazione rappresentano i servizi di autenticazione passati a varie funzioni di run-time.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518724"
---
# <a name="authentication-service-constants"></a><span data-ttu-id="0f944-103">Costanti Authentication-Service</span><span class="sxs-lookup"><span data-stu-id="0f944-103">Authentication-Service Constants</span></span>

<span data-ttu-id="0f944-104">Le costanti del servizio di autenticazione rappresentano i servizi di autenticazione passati a varie funzioni di run-time.</span><span class="sxs-lookup"><span data-stu-id="0f944-104">The authentication service constants represent the authentication services passed to various run-time functions.</span></span>

<span data-ttu-id="0f944-105">Le costanti seguenti sono valori validi per il parametro *AuthnSvc* .</span><span class="sxs-lookup"><span data-stu-id="0f944-105">The following constants are valid values for the *AuthnSvc* parameter.</span></span>



| <span data-ttu-id="0f944-106">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="0f944-106">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="0f944-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f944-107">Description</span></span>                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <span data-ttu-id="0f944-108"><dt>**RPC \_ \_Autenticazione C \_ Nessuna**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-108"><dt>**RPC\_C\_AUTHN\_NONE**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="0f944-109">Nessuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="0f944-109">No authentication.</span></span><br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <span data-ttu-id="0f944-110"><dt>**RPC \_ C \_ AuthN \_ DCE \_ privato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-110"><dt>**RPC\_C\_AUTHN\_DCE\_PRIVATE**</dt> <dt>1</dt></span></span> </dl>        | <span data-ttu-id="0f944-111">Usare l'autenticazione con chiave privata DCE (Distributed Computing Environment).</span><span class="sxs-lookup"><span data-stu-id="0f944-111">Use Distributed Computing Environment (DCE) private key authentication.</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <span data-ttu-id="0f944-112"><dt>**RPC \_ Autorità di \_ autenticazione \_ DCE C \_ pubblica**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-112"><dt>**RPC\_C\_AUTHN\_DCE\_PUBLIC**</dt> <dt>2</dt></span></span> </dl>           | <span data-ttu-id="0f944-113">Autenticazione con chiave pubblica DCE (riservata per uso futuro).</span><span class="sxs-lookup"><span data-stu-id="0f944-113">DCE public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <span data-ttu-id="0f944-114"><dt>**RPC \_ C \_ AuthN \_ dicembre \_ pubblico**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-114"><dt>**RPC\_C\_AUTHN\_DEC\_PUBLIC**</dt> <dt>4</dt></span></span> </dl>           | <span data-ttu-id="0f944-115">Autenticazione con chiave pubblica DEC (riservata per uso futuro).</span><span class="sxs-lookup"><span data-stu-id="0f944-115">DEC public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <span data-ttu-id="0f944-116"><dt>**RPC \_ C \_ AuthN \_ GSS \_ Negotiate**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-116"><dt>**RPC\_C\_AUTHN\_GSS\_NEGOTIATE**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="0f944-117">Utilizzare [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span><span class="sxs-lookup"><span data-stu-id="0f944-117">Use the [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span></span> <span data-ttu-id="0f944-118">Questo SSP negozia tra l'utilizzo dei provider di supporto per la sicurezza (SSP) del protocollo NTLM e Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0f944-118">This SSP negotiates between the use of the NTLM and Kerberos protocol Security Support Providers (SSP).</span></span><br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <span data-ttu-id="0f944-119"><dt>**RPC \_ \_ \_ WinNT auth**</dt> <dt>10</dt> di C</span><span class="sxs-lookup"><span data-stu-id="0f944-119"><dt>**RPC\_C\_AUTHN\_WINNT**</dt> <dt>10</dt></span></span> </dl>                          | <span data-ttu-id="0f944-120">Utilizzare il [provider di servizi condivisi di Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).</span><span class="sxs-lookup"><span data-stu-id="0f944-120">Use the [Microsoft NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm).</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <span data-ttu-id="0f944-121"><dt>**RPC \_ C \_ AuthN \_ GSS \_ Schannel**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-121"><dt>**RPC\_C\_AUTHN\_GSS\_SCHANNEL**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="0f944-122">Usare [SSP Schannel](/windows/desktop/SecAuthN/secure-channel).</span><span class="sxs-lookup"><span data-stu-id="0f944-122">Use the [Schannel SSP](/windows/desktop/SecAuthN/secure-channel).</span></span> <span data-ttu-id="0f944-123">Questo SSP supporta Secure Socket Layer (SSL), la tecnologia di comunicazione privata (PCT) e la sicurezza a livello di trasporto (TLS).</span><span class="sxs-lookup"><span data-stu-id="0f944-123">This SSP supports Secure Socket Layer (SSL), private communication technology (PCT), and transport level security (TLS).</span></span><br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <span data-ttu-id="0f944-124"><dt>**RPC \_ Autenticazione del linguaggio C ( \_ \_ \_ Kerberos**</dt> ) a <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-124"><dt>**RPC\_C\_AUTHN\_GSS\_KERBEROS**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="0f944-125">Utilizzare [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span><span class="sxs-lookup"><span data-stu-id="0f944-125">Use the [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span></span><br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <span data-ttu-id="0f944-126"><dt>**RPC \_ \_Autenticazione \_ DPA**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0f944-126"><dt>**RPC\_C\_AUTHN\_DPA**</dt> <dt>17</dt></span></span> </dl>                                | <span data-ttu-id="0f944-127">Usare l'autenticazione della password distribuita (DPA).</span><span class="sxs-lookup"><span data-stu-id="0f944-127">Use Distributed Password Authentication (DPA).</span></span><br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <span data-ttu-id="0f944-128"><dt>**RPC \_ \_MSN AuthN \_ MSN**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-128"><dt>**RPC\_C\_AUTHN\_MSN**</dt> <dt>18</dt></span></span> </dl>                                | <span data-ttu-id="0f944-129">SSP del protocollo di autenticazione usato per la rete Microsoft (MSN).</span><span class="sxs-lookup"><span data-stu-id="0f944-129">Authentication protocol SSP used for the Microsoft Network (MSN).</span></span><br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <span data-ttu-id="0f944-130"><dt>**RPC \_ \_ \_ Digest di autenticazione C**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-130"><dt>**RPC\_C\_AUTHN\_DIGEST**</dt> <dt>21</dt></span></span> </dl>                       | <span data-ttu-id="0f944-131">Windows XP o versione successiva: usare [SSP Microsoft Digest](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span><span class="sxs-lookup"><span data-stu-id="0f944-131">Windows XP or later: Use the [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span></span><br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <span data-ttu-id="0f944-132"><dt>**RPC \_ \_ \_ Nego \_ Extender**</dt> <dt>30</dt> di autenticazione C</span><span class="sxs-lookup"><span data-stu-id="0f944-132"><dt>**RPC\_C\_AUTHN\_NEGO\_EXTENDER**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="0f944-133">Windows 7 o versioni successive: riservato.</span><span class="sxs-lookup"><span data-stu-id="0f944-133">Windows 7 or later: Reserved.</span></span> <span data-ttu-id="0f944-134">Non utilizzare</span><span class="sxs-lookup"><span data-stu-id="0f944-134">Do not use</span></span><br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <span data-ttu-id="0f944-135"><dt>**RPC \_ C \_ AuthN \_ mq**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-135"><dt>**RPC\_C\_AUTHN\_MQ**</dt> <dt>100</dt></span></span> </dl>                                  | <span data-ttu-id="0f944-136">Questo SSP fornisce un wrapper compatibile con SSPI per il protocollo a livello di trasporto di Microsoft Message Queue (MSMQ).</span><span class="sxs-lookup"><span data-stu-id="0f944-136">This SSP provides an SSPI-compatible wrapper for the Microsoft Message Queue (MSMQ) transport-level protocol.</span></span><br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <span data-ttu-id="0f944-137"><dt>**RPC \_ 0xFFFFFFFF \_ \_ predefinito di autenticazione C**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0f944-137"><dt>**RPC\_C\_AUTHN\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl>            | <span data-ttu-id="0f944-138">Usare il servizio di autenticazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="0f944-138">Use the default authentication service.</span></span><br/>                                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="0f944-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f944-139">Remarks</span></span>

<span data-ttu-id="0f944-140">Specificare RPC \_ C \_ AuthN \_ None per disattivare l'autenticazione per le chiamate di procedure remote effettuate su un handle di binding.</span><span class="sxs-lookup"><span data-stu-id="0f944-140">Specify RPC\_C\_AUTHN\_NONE to turn off authentication for remote procedure calls made over a binding handle.</span></span> <span data-ttu-id="0f944-141">Quando si specifica l' \_ impostazione predefinita per l'autenticazione RPC c \_ \_ , la libreria di runtime RPC USA \_ il \_ \_ servizio di autenticazione WinNT c AuthN per le chiamate di procedure remote effettuate usando l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="0f944-141">When you specify RPC\_C\_AUTHN\_DEFAULT, the RPC run-time library uses the RPC\_C\_AUTHN\_WINNT authentication service for remote procedure calls made using the binding handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f944-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f944-142">Requirements</span></span>



| <span data-ttu-id="0f944-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f944-143">Requirement</span></span> | <span data-ttu-id="0f944-144">Valore</span><span class="sxs-lookup"><span data-stu-id="0f944-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f944-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f944-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0f944-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f944-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f944-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f944-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0f944-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f944-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f944-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f944-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f944-150"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f944-150"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f944-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f944-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f944-152">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="0f944-152">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="0f944-153">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="0f944-153">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="0f944-154">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="0f944-154">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="0f944-155">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="0f944-155">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="0f944-156">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="0f944-156">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="0f944-157">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="0f944-157">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

