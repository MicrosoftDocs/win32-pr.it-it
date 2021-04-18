---
title: '\_Req creda EAP \_ (Eaptypes. h)'
description: Archivia le credenziali di sicurezza EAP in una \_ struttura di matrice di campi di input di configurazione EAP \_ \_ \_ . | \_Req creda EAP \_ (Eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321620"
---
# <a name="eap_cred_req"></a><span data-ttu-id="2e1ab-105">\_req creda EAP \_</span><span class="sxs-lookup"><span data-stu-id="2e1ab-105">EAP\_CRED\_REQ</span></span>

<span data-ttu-id="2e1ab-106">La struttura della richiesta **EAP \_ cred \_** archivia le credenziali di sicurezza EAP in una struttura di [**matrice di campi di \_ input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="2e1ab-106">The **EAP\_CRED\_REQ** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

<span data-ttu-id="2e1ab-107">**\_req creda EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2e1ab-107">**EAP\_CRED\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="2e1ab-108">La struttura della richiesta **EAP \_ cred \_** archivia sia la vecchia che la nuova credenziale di sicurezza EAP a cui punta il parametro *pbUiData* della struttura di [**dati dell' \_ \_ interfaccia utente \_ di EAP Interactive**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il parametro *dwDataType* del tipo di [**\_ \_ \_ dati \_ dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di richiesta di credenziale.</span><span class="sxs-lookup"><span data-stu-id="2e1ab-108">The **EAP\_CRED\_REQ** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e1ab-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e1ab-109">Remarks</span></span>

<span data-ttu-id="2e1ab-110">Per supportare l'accesso Single Sign-on (SSO), viene utilizzata la struttura di **\_ \_ req creda EAP** .</span><span class="sxs-lookup"><span data-stu-id="2e1ab-110">The **EAP\_CRED\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="2e1ab-111">La struttura di **\_ \_ req creda EAP** è identica alla struttura [**EAP \_ cred \_**](eap-cred-resp.md) .</span><span class="sxs-lookup"><span data-stu-id="2e1ab-111">The **EAP\_CRED\_REQ** structure is identical to the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1ab-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e1ab-112">Requirements</span></span>



| <span data-ttu-id="2e1ab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e1ab-113">Requirement</span></span> | <span data-ttu-id="2e1ab-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2e1ab-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e1ab-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e1ab-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1ab-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e1ab-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e1ab-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e1ab-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1ab-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e1ab-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e1ab-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e1ab-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e1ab-120"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e1ab-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e1ab-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e1ab-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1ab-122">Strutture supplicant EAPHost</span><span class="sxs-lookup"><span data-stu-id="2e1ab-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="2e1ab-123">**\_creda \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="2e1ab-123">**EAP\_CRED\_RESP**</span></span>](eap-cred-resp.md)
</dt> <dt>

[<span data-ttu-id="2e1ab-124">**REQ di scadenza di EAP \_ cred \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2e1ab-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="2e1ab-125">[**la \_ scadenza del credito EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2e1ab-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2e1ab-126">**\_ \_ dati dell'interfaccia utente interattiva EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2e1ab-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="2e1ab-127">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="2e1ab-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

