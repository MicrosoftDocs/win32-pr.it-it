---
title: '\_ \_ Accesso resp EAP \_ (Eaptypes. h)'
description: Archivia le credenziali di sicurezza EAP in una \_ struttura di matrice di campi di input di configurazione EAP \_ \_ \_ . | \_ \_ Accesso resp EAP \_ (Eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321621"
---
# <a name="eap_cred_logon_resp"></a><span data-ttu-id="3a6b1-105">\_ \_ accesso \_ resp EAP</span><span class="sxs-lookup"><span data-stu-id="3a6b1-105">EAP\_CRED\_LOGON\_RESP</span></span>

<span data-ttu-id="3a6b1-106">La struttura di **\_ \_ accesso \_ resp EAP di EAP** archivia le credenziali di sicurezza EAP in una struttura di matrice di [**\_ campi di input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="3a6b1-106">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

<span data-ttu-id="3a6b1-107">**\_ \_ accesso \_ resp EAP**</span><span class="sxs-lookup"><span data-stu-id="3a6b1-107">**EAP\_CRED\_LOGON\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="3a6b1-108">La struttura di **\_ \_ accesso \_ resp di EAP** consente di archiviare le credenziali di sicurezza EAP a cui punta il parametro *pbUiData* della struttura di [**\_ \_ \_ dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il parametro *dwDataType* del [**tipo di \_ \_ \_ dati \_ dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di richiesta di credenziale.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-108">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="3a6b1-109">I campi di input in questa struttura saranno uguali ai campi di input restituiti da [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span><span class="sxs-lookup"><span data-stu-id="3a6b1-109">The input fields in this structure will be same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="3a6b1-110">**EAP \_ Il valore di \_ accesso cred \_** viene usato nella richiesta di credenziali iniziale e il valore [**EAP \_ cred \_**](eap-cred-resp.md) è usato nella richiesta di ripetizione delle credenziali durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3a6b1-110">**EAP\_CRED\_LOGON\_RESP** is used in the initial credential request and [**EAP\_CRED\_RESP**](eap-cred-resp.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a6b1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a6b1-111">Remarks</span></span>

<span data-ttu-id="3a6b1-112">Per supportare single sign-on (SSO) viene utilizzata la struttura di **\_ \_ accesso \_ resp EAP** .</span><span class="sxs-lookup"><span data-stu-id="3a6b1-112">The **EAP\_CRED\_LOGON\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="3a6b1-113">La struttura di **\_ \_ accesso \_ resp di EAP creda** è identica alla struttura di [**\_ \_ \_ req di accesso di EAP cred**](eap-cred-logon-req.md) .</span><span class="sxs-lookup"><span data-stu-id="3a6b1-113">The **EAP\_CRED\_LOGON\_RESP** structure is identical to the [**EAP\_CRED\_LOGON\_REQ**](eap-cred-logon-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a6b1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a6b1-114">Requirements</span></span>



| <span data-ttu-id="3a6b1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a6b1-115">Requirement</span></span> | <span data-ttu-id="3a6b1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3a6b1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6b1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a6b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3a6b1-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a6b1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a6b1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a6b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3a6b1-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a6b1-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a6b1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a6b1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a6b1-122"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a6b1-122"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a6b1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a6b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6b1-124">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="3a6b1-124">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[<span data-ttu-id="3a6b1-125">**\_matrice di \_ campi di input configurazione \_ EAP \_**</span><span class="sxs-lookup"><span data-stu-id="3a6b1-125">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="3a6b1-126">**richiesta di accesso di EAP \_ cred \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3a6b1-126">**EAP\_CRED\_LOGON\_REQ**</span></span>](eap-cred-logon-req.md)
</dt> <dt>

[<span data-ttu-id="3a6b1-127">**\_ \_ dati dell'interfaccia utente interattiva EAP \_**</span><span class="sxs-lookup"><span data-stu-id="3a6b1-127">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="3a6b1-128">**\_tipo di \_ dati dell'interfaccia utente interattiva EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3a6b1-128">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





