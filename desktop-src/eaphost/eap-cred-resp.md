---
title: '\_Creda EAP \_ (Eaptypes. h)'
description: Archivia le credenziali di sicurezza EAP in una \_ struttura di matrice di campi di input di configurazione EAP \_ \_ \_ . | \_Creda EAP \_ (Eaptypes. h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c2176377dbde0f7c02d2a7d8083ad1bcff9e71
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321200"
---
# <a name="eap_cred_resp"></a><span data-ttu-id="b2062-105">\_creda \_ EAP</span><span class="sxs-lookup"><span data-stu-id="b2062-105">EAP\_CRED\_RESP</span></span>

<span data-ttu-id="b2062-106">La struttura **EAP cred. consente \_ \_** di archiviare le credenziali di sicurezza EAP in una struttura di [**matrice di campi di \_ input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .</span><span class="sxs-lookup"><span data-stu-id="b2062-106">The **EAP\_CRED\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

<span data-ttu-id="b2062-107">**\_creda \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="b2062-107">**EAP\_CRED\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="b2062-108">Nella struttura **EAP \_ creda \_** è possibile archiviare sia la vecchia che la nuova credenziale di sicurezza EAP a cui punta il parametro *pbUiData* della struttura di [**\_ \_ \_ dati dell'interfaccia utente interattiva EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando il parametro *dwDataType* del [**tipo di dati di EAP \_ Interactive \_ UI \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifica un tipo di risposta delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="b2062-108">The **EAP\_CRED\_RESP** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential response type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2062-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2062-109">Remarks</span></span>

<span data-ttu-id="b2062-110">Per supportare single sign-on (SSO), viene usata la struttura **EAP \_ cred \_** .</span><span class="sxs-lookup"><span data-stu-id="b2062-110">The **EAP\_CRED\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="b2062-111">La struttura di **EAP \_ creda \_** è identica alla struttura della richiesta [**EAP \_ cred \_**](eap-cred-req.md) .</span><span class="sxs-lookup"><span data-stu-id="b2062-111">The **EAP\_CRED\_RESP** structure is identical to the [**EAP\_CRED\_REQ**](eap-cred-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2062-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2062-112">Requirements</span></span>



| <span data-ttu-id="b2062-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2062-113">Requirement</span></span> | <span data-ttu-id="b2062-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b2062-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2062-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2062-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b2062-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2062-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2062-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2062-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b2062-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2062-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2062-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2062-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2062-120"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2062-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2062-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2062-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2062-122">Strutture supplicant EAPHost</span><span class="sxs-lookup"><span data-stu-id="b2062-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="b2062-123">**\_req creda EAP \_**</span><span class="sxs-lookup"><span data-stu-id="b2062-123">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="b2062-124">**REQ di scadenza di EAP \_ cred \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b2062-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="b2062-125">[**la \_ scadenza del credito EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2062-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b2062-126">**\_ \_ dati dell'interfaccia utente interattiva EAP \_**</span><span class="sxs-lookup"><span data-stu-id="b2062-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="b2062-127">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="b2062-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

