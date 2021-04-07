---
title: REQ di accesso di EAP \_ cred \_ \_ (Eaptypes. h)
description: Archivia le credenziali di sicurezza EAP in una \_ struttura di matrice di campi di input di configurazione EAP \_ \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048132"
---
# <a name="eap_cred_logon_req"></a><span data-ttu-id="02598-104">richiesta di accesso di EAP \_ cred \_ \_</span><span class="sxs-lookup"><span data-stu-id="02598-104">EAP\_CRED\_LOGON\_REQ</span></span>

<span data-ttu-id="02598-105">La struttura di richiesta di **accesso di EAP \_ cred \_ \_** archivia le credenziali di sicurezza EAP in una struttura di matrice di campi di [**input di \_ configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="02598-105">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials within an [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

<span data-ttu-id="02598-106">**richiesta di accesso di EAP \_ cred \_ \_**</span><span class="sxs-lookup"><span data-stu-id="02598-106">**EAP\_CRED\_LOGON\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="02598-107">La struttura di **req di accesso di EAP \_ \_ \_ cred** archivia le credenziali di sicurezza EAP a cui punta il parametro *pbUiData* della struttura di [**\_ \_ \_ dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il parametro *dwDataType* del tipo di [**\_ \_ \_ dati \_ dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di richiesta di credenziale.</span><span class="sxs-lookup"><span data-stu-id="02598-107">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="02598-108">I campi di input in questa struttura sono gli stessi dei campi di input restituiti da [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="02598-108">The input fields in this structure are the same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="02598-109">**EAP \_ La richiesta di \_ accesso cred \_** viene usata nella richiesta di credenziali iniziale e la richiesta [**EAP \_ creda \_**](eap-cred-req.md) viene usata nella richiesta di ripetizione delle credenziali durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="02598-109">**EAP\_CRED\_LOGON\_REQ** is used in the initial credential request and [**EAP\_CRED\_REQ**](eap-cred-req.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02598-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="02598-110">Remarks</span></span>

<span data-ttu-id="02598-111">Per supportare l'accesso Single Sign-on (SSO), viene usata la struttura di **\_ req di \_ accesso \_ di EAP cred** .</span><span class="sxs-lookup"><span data-stu-id="02598-111">The **EAP\_CRED\_LOGON\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="02598-112">La struttura della richiesta di **accesso di EAP \_ cred \_ \_** è identica alla struttura di [**\_ \_ accesso \_ resp di EAP cred**](eap-cred-logon-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="02598-112">The **EAP\_CRED\_LOGON\_REQ** structure is identical to the [**EAP\_CRED\_LOGON\_RESP**](eap-cred-logon-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="02598-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02598-113">Requirements</span></span>



| <span data-ttu-id="02598-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="02598-114">Requirement</span></span> | <span data-ttu-id="02598-115">Valore</span><span class="sxs-lookup"><span data-stu-id="02598-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02598-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02598-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02598-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02598-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02598-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02598-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02598-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="02598-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="02598-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02598-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02598-121"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="02598-121"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02598-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02598-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02598-123">**\_matrice di \_ campi di input configurazione \_ EAP \_**</span><span class="sxs-lookup"><span data-stu-id="02598-123">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="02598-124">**\_req creda EAP \_**</span><span class="sxs-lookup"><span data-stu-id="02598-124">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="02598-125">**\_ \_ dati dell'interfaccia utente interattiva EAP \_**</span><span class="sxs-lookup"><span data-stu-id="02598-125">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="02598-126">**\_tipo di \_ dati dell'interfaccia utente interattiva EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="02598-126">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[<span data-ttu-id="02598-127">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="02598-127">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





