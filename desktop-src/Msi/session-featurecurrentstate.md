---
description: La proprietà FeatureCurrentState dell'oggetto Session è una proprietà di sola lettura che restituisce lo stato di installazione corrente della funzionalità designata. Per i valori di stato, vedere la proprietà FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Proprietà Session. FeatureCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329105"
---
# <a name="sessionfeaturecurrentstate-property"></a><span data-ttu-id="2fed9-104">Proprietà Session. FeatureCurrentState</span><span class="sxs-lookup"><span data-stu-id="2fed9-104">Session.FeatureCurrentState property</span></span>

<span data-ttu-id="2fed9-105">La proprietà **FeatureCurrentState** dell'oggetto [**Session**](session-object.md) è una proprietà di sola lettura che restituisce lo stato di installazione corrente della funzionalità designata.</span><span class="sxs-lookup"><span data-stu-id="2fed9-105">The **FeatureCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated feature.</span></span> <span data-ttu-id="2fed9-106">Per i valori di stato, vedere la proprietà [**FeatureRequestState**](session-featurerequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="2fed9-106">For state values, see the [**FeatureRequestState**](session-featurerequeststate.md) property.</span></span>

<span data-ttu-id="2fed9-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2fed9-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fed9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fed9-108">Syntax</span></span>


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a><span data-ttu-id="2fed9-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2fed9-109">Property value</span></span>

<span data-ttu-id="2fed9-110">Nome della stringa obbligatoria della funzionalità richiesta e una chiave primaria nella tabella delle [funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fed9-110">Required string name of the requested feature, and a primary key into the [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fed9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fed9-111">Remarks</span></span>

<span data-ttu-id="2fed9-112">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="2fed9-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fed9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fed9-113">Requirements</span></span>



| <span data-ttu-id="2fed9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fed9-114">Requirement</span></span> | <span data-ttu-id="2fed9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2fed9-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fed9-116">Versione</span><span class="sxs-lookup"><span data-stu-id="2fed9-116">Version</span></span><br/> | <span data-ttu-id="2fed9-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2fed9-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2fed9-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2fed9-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2fed9-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="2fed9-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2fed9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2fed9-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="2fed9-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fed9-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2fed9-122">IID</span><span class="sxs-lookup"><span data-stu-id="2fed9-122">IID</span></span><br/>     | <span data-ttu-id="2fed9-123">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2fed9-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="2fed9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fed9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fed9-125">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="2fed9-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="2fed9-126">**Proprietà FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="2fed9-126">**FeatureRequestState property**</span></span>](session-featurerequeststate.md)
</dt> </dl>

 

 




