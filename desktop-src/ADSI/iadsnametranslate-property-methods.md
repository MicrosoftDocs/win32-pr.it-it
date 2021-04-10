---
title: Metodi di proprietà IADsNameTranslate (IADs. h)
description: Imposta la proprietà ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsNameTranslate ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964659"
---
# <a name="iadsnametranslate-property-methods"></a><span data-ttu-id="9f12e-104">Metodi di proprietà IADsNameTranslate</span><span class="sxs-lookup"><span data-stu-id="9f12e-104">IADsNameTranslate Property Methods</span></span>

<span data-ttu-id="9f12e-105">Il metodo Property dell'interfaccia [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) imposta la proprietà **ChaseReferral** .</span><span class="sxs-lookup"><span data-stu-id="9f12e-105">The property method of the [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface sets the **ChaseReferral** property.</span></span> <span data-ttu-id="9f12e-106">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9f12e-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9f12e-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f12e-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9f12e-108">**ChaseReferral**</span><span class="sxs-lookup"><span data-stu-id="9f12e-108">**ChaseReferral**</span></span>
<span data-ttu-id="9f12e-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9f12e-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="9f12e-110">Opzioni di ricerca dei riferimenti come definito in [**Ads \_ Chase \_ rinvii \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span><span class="sxs-lookup"><span data-stu-id="9f12e-110">Options of referral chasing as defined in [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span></span> <span data-ttu-id="9f12e-111">Quando viene impostata l'indicizzazione del riferimento, la conversione del nome viene eseguita sugli oggetti che non appartengono a questa directory e sono i riferimenti restituiti dalla ricerca dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="9f12e-111">When referral chasing is set, the name translation is performed on objects that do not belong to this directory and are the referrals returned from referral chasing.</span></span>

<dt>

<span data-ttu-id="9f12e-112">Tipo di accesso: sola scrittura</span><span class="sxs-lookup"><span data-stu-id="9f12e-112">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="9f12e-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="9f12e-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="9f12e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f12e-114">Remarks</span></span>

<span data-ttu-id="9f12e-115">Le opzioni di Chasing per il riferimento si applicano solo quando si usano [**IADsNameTranslate:: set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) e [**IADsNameTranslate:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span><span class="sxs-lookup"><span data-stu-id="9f12e-115">The referral chasing options apply only when you use [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) and [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span></span> <span data-ttu-id="9f12e-116">La funzionalità non è disponibile con [**IADsNameTranslate:: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) o [**IADsNameTranslate:: GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span><span class="sxs-lookup"><span data-stu-id="9f12e-116">The feature is not available with [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) or [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span></span>

<span data-ttu-id="9f12e-117">L'interfaccia [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) ha un'implementazione parziale di [**Ads \_ Chase \_ referrals \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) tramite la proprietà **ChaseReferral** .</span><span class="sxs-lookup"><span data-stu-id="9f12e-117">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface has a partial implementation of [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) through the **ChaseReferral** property.</span></span> <span data-ttu-id="9f12e-118">Se la proprietà **ChaseReferral** è impostata su zero (0), equivale a specificare i **\_ riferimenti Chase di ADS \_ \_ mai** (0).</span><span class="sxs-lookup"><span data-stu-id="9f12e-118">If the **ChaseReferral** property is set to zero (0), it is the same as specifying **ADS\_CHASE\_REFERRALS\_NEVER** (0).</span></span> <span data-ttu-id="9f12e-119">Se viene usato un valore diverso da zero, equivale a specificare i **\_ riferimenti Chase di ADS \_ \_ Always** (0x60).</span><span class="sxs-lookup"><span data-stu-id="9f12e-119">If a nonzero value is used, it is the same as specifying **ADS\_CHASE\_REFERRALS\_ALWAYS** (0x60).</span></span> <span data-ttu-id="9f12e-120">**IADsNameTranslate** non implementa le opzioni **Ads \_ Chase \_ \_ subordinate** (0x20) o **Ads \_ Chase \_ \_ External** (0x40).</span><span class="sxs-lookup"><span data-stu-id="9f12e-120">**IADsNameTranslate** does not implement the **ADS\_CHASE\_REFERRALS\_SUBORDINATE** (0x20) or **ADS\_CHASE\_REFERRALS\_EXTERNAL** (0x40) options.</span></span>

<span data-ttu-id="9f12e-121">L'impostazione predefinita per l'inseguimento dei riferimenti è abilitata (**Ads \_ Chase si \_ riferisce \_ sempre**).</span><span class="sxs-lookup"><span data-stu-id="9f12e-121">The default setting for referral chasing is enabled (**ADS\_CHASE\_REFERRALS\_ALWAYS**).</span></span> <span data-ttu-id="9f12e-122">Senza la ricerca di riferimenti, è possibile eseguire la conversione dei nomi su tali oggetti che risiedono solo nel server di directory connesso.</span><span class="sxs-lookup"><span data-stu-id="9f12e-122">Without referral chasing, you can have name translation performed on those objects residing on the connected directory server only.</span></span> <span data-ttu-id="9f12e-123">Se non si è certi che l'oggetto di interesse si trovi nel server specificato, è necessario impostare questa proprietà in modo che sia **\_ \_ \_ sempre ADS Chase referrals**.</span><span class="sxs-lookup"><span data-stu-id="9f12e-123">If you are uncertain whether the object of interest is on the specified server, you should set this property to be **ADS\_CHASE\_REFERRALS\_ALWAYS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f12e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f12e-124">Requirements</span></span>



| <span data-ttu-id="9f12e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f12e-125">Requirement</span></span> | <span data-ttu-id="9f12e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9f12e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f12e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f12e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9f12e-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f12e-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f12e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f12e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9f12e-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f12e-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f12e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f12e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f12e-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f12e-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="9f12e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9f12e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f12e-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f12e-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="9f12e-135">IID</span><span class="sxs-lookup"><span data-stu-id="9f12e-135">IID</span></span><br/>                      | <span data-ttu-id="9f12e-136">IID \_ IADsNameTranslate è definito come B1B272A3-3625-11D1-A3A4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="9f12e-136">IID\_IADsNameTranslate is defined as B1B272A3-3625-11D1-A3A4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="9f12e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f12e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f12e-138">**\_enumerazione riferimenti inseguiti Ads \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9f12e-138">**ADS\_CHASE\_REFERRALS\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[<span data-ttu-id="9f12e-139">**IADsNameTranslate**</span><span class="sxs-lookup"><span data-stu-id="9f12e-139">**IADsNameTranslate**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[<span data-ttu-id="9f12e-140">**IADsNameTranslate:: Get**</span><span class="sxs-lookup"><span data-stu-id="9f12e-140">**IADsNameTranslate::Get**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[<span data-ttu-id="9f12e-141">**IADsNameTranslate::GetEx**</span><span class="sxs-lookup"><span data-stu-id="9f12e-141">**IADsNameTranslate::GetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[<span data-ttu-id="9f12e-142">**IADsNameTranslate:: set**</span><span class="sxs-lookup"><span data-stu-id="9f12e-142">**IADsNameTranslate::Set**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[<span data-ttu-id="9f12e-143">**IADsNameTranslate:: SetEx**</span><span class="sxs-lookup"><span data-stu-id="9f12e-143">**IADsNameTranslate::SetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[<span data-ttu-id="9f12e-144">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="9f12e-144">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





