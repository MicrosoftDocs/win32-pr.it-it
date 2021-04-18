---
description: La proprietà FeatureUsageDate è una proprietà di sola lettura che restituisce la data dell'ultima utilizzo della funzionalità specificata.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Proprietà Installer. FeatureUsageDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324630"
---
# <a name="installerfeatureusagedate-property"></a><span data-ttu-id="d430e-103">Proprietà Installer. FeatureUsageDate</span><span class="sxs-lookup"><span data-stu-id="d430e-103">Installer.FeatureUsageDate property</span></span>

<span data-ttu-id="d430e-104">La proprietà **FeatureUsageDate** è una proprietà di sola lettura che restituisce la data dell'ultima utilizzo della funzionalità specificata.</span><span class="sxs-lookup"><span data-stu-id="d430e-104">The **FeatureUsageDate** property is a read-only property that returns the date the specified feature was last used.</span></span>

<span data-ttu-id="d430e-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d430e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d430e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d430e-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a><span data-ttu-id="d430e-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d430e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d430e-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d430e-108">Remarks</span></span>

<span data-ttu-id="d430e-109">L'uso dei metodi [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o i relativi equivalenti API nella funzionalità specificata consente di impostare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="d430e-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature sets this property.</span></span>

<span data-ttu-id="d430e-110">La data è nel formato di data MS-DOS, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d430e-110">The date is in the MS-DOS date format as shown in the following table.</span></span>



| <span data-ttu-id="d430e-111">BITS</span><span class="sxs-lookup"><span data-stu-id="d430e-111">Bits</span></span> | <span data-ttu-id="d430e-112">Contenuto</span><span class="sxs-lookup"><span data-stu-id="d430e-112">Contents</span></span>                                            |
|------|-----------------------------------------------------|
| <span data-ttu-id="d430e-113">0-4</span><span class="sxs-lookup"><span data-stu-id="d430e-113">0-4</span></span>  | <span data-ttu-id="d430e-114">Giorno del mese (1-31)</span><span class="sxs-lookup"><span data-stu-id="d430e-114">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="d430e-115">5-8</span><span class="sxs-lookup"><span data-stu-id="d430e-115">5-8</span></span>  | <span data-ttu-id="d430e-116">Month (1 = gennaio, 2 = febbraio e così via)</span><span class="sxs-lookup"><span data-stu-id="d430e-116">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="d430e-117">9-15</span><span class="sxs-lookup"><span data-stu-id="d430e-117">9-15</span></span> | <span data-ttu-id="d430e-118">Offset anno da 1980 (aggiungere 1980 per ottenere l'anno effettivo)</span><span class="sxs-lookup"><span data-stu-id="d430e-118">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d430e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d430e-119">Requirements</span></span>



| <span data-ttu-id="d430e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d430e-120">Requirement</span></span> | <span data-ttu-id="d430e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d430e-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d430e-122">Versione</span><span class="sxs-lookup"><span data-stu-id="d430e-122">Version</span></span><br/> | <span data-ttu-id="d430e-123">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d430e-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d430e-124">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d430e-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d430e-125">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="d430e-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d430e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d430e-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="d430e-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d430e-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d430e-128">IID</span><span class="sxs-lookup"><span data-stu-id="d430e-128">IID</span></span><br/>     | <span data-ttu-id="d430e-129">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d430e-129">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="d430e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d430e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d430e-131">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="d430e-131">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




