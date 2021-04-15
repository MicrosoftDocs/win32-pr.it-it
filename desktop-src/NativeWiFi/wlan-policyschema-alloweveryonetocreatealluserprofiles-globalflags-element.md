---
description: Specifica se un utente può creare un profilo per tutti gli utenti.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: Elemento allowEveryoneToCreateAllUserProfiles (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525765"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a><span data-ttu-id="aa351-103">Elemento allowEveryoneToCreateAllUserProfiles (globalFlags)</span><span class="sxs-lookup"><span data-stu-id="aa351-103">allowEveryoneToCreateAllUserProfiles (globalFlags) Element</span></span>

<span data-ttu-id="aa351-104">L'elemento **allowEveryoneToCreateAllUserProfiles** (globalFlags) specifica se un utente può creare un profilo per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="aa351-104">The **allowEveryoneToCreateAllUserProfiles** (globalFlags) element specifies whether any user can create an all-user profile.</span></span> <span data-ttu-id="aa351-105">Un profilo utente tutti può essere usato da qualsiasi utente nel computer per connettersi alla rete wireless associata al profilo.</span><span class="sxs-lookup"><span data-stu-id="aa351-105">An all-user profile can be used by any user on the machine to connect to the wireless network associated with the profile.</span></span>

<span data-ttu-id="aa351-106">Se **allowEveryoneToCreateAllUserProfiles** è true, qualsiasi utente può creare un profilo per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="aa351-106">If **allowEveryoneToCreateAllUserProfiles** is TRUE, than any user can create an all-user profile.</span></span> <span data-ttu-id="aa351-107">Se **allowEveryoneToCreateAllUserProfiles** è false, non tutti gli utenti possono creare un profilo per tutti gli utenti ed è disponibile un DACL associato all'oggetto di \_ \_ sicurezza Aggiungi \_ nuovo tutti i profili utente di WLAN Secure, \_ \_ \_ che specifica gli utenti o i gruppi di utenti con l'autorizzazione per la creazione di tutti i profili utente.</span><span class="sxs-lookup"><span data-stu-id="aa351-107">If **allowEveryoneToCreateAllUserProfiles** is FALSE, then not all users can create an all-user profile, and there is a DACL associated with the wlan\_secure\_add\_new\_all\_user\_profiles security object that specifies the users or user groups with permission to create all-user profiles.</span></span> <span data-ttu-id="aa351-108">Il DACL predefinito specifica che solo gli utenti che hanno eseguito l'accesso come membro del gruppo Administrators possono creare un profilo per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="aa351-108">The default DACL specifies that only users that are logged on as a member of the Administrators group can create an all-user profile.</span></span> <span data-ttu-id="aa351-109">Le impostazioni di sicurezza predefinite possono essere modificate chiamando [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="aa351-109">The default security settings can be changed by calling [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span></span> <span data-ttu-id="aa351-110">Per ottenere le impostazioni di sicurezza correnti, chiamare [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="aa351-110">To get the current security settings, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="aa351-111">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa351-111">This element is mandatory.</span></span> <span data-ttu-id="aa351-112">Quando un profilo viene creato dal servizio di configurazione automatica, questo elemento avrà il valore predefinito TRUE.</span><span class="sxs-lookup"><span data-stu-id="aa351-112">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

<span data-ttu-id="aa351-113">L'elemento **allowEveryoneToCreateAllUserProfiles** è definito dall'elemento [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aa351-113">The **allowEveryoneToCreateAllUserProfiles** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa351-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa351-114">Requirements</span></span>



| <span data-ttu-id="aa351-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa351-115">Requirement</span></span> | <span data-ttu-id="aa351-116">Valore</span><span class="sxs-lookup"><span data-stu-id="aa351-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa351-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa351-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa351-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa351-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa351-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa351-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa351-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa351-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa351-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa351-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa351-122">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="aa351-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="aa351-123">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="aa351-123">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="aa351-124">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="aa351-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="aa351-125">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="aa351-125">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




