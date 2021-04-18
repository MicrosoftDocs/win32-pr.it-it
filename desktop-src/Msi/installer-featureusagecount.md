---
description: La proprietà FeatureUsageCount è una proprietà di sola lettura che restituisce il numero di volte in cui la funzionalità è stata utilizzata.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Proprietà Installer. FeatureUsageCount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324634"
---
# <a name="installerfeatureusagecount-property"></a><span data-ttu-id="7799c-103">Proprietà Installer. FeatureUsageCount</span><span class="sxs-lookup"><span data-stu-id="7799c-103">Installer.FeatureUsageCount property</span></span>

<span data-ttu-id="7799c-104">La proprietà **FeatureUsageCount** è una proprietà di sola lettura che restituisce il numero di volte in cui la funzionalità è stata utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7799c-104">The **FeatureUsageCount** property is a read-only property that returns the number of times the feature has been used.</span></span>

<span data-ttu-id="7799c-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7799c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7799c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7799c-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a><span data-ttu-id="7799c-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7799c-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7799c-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="7799c-108">Remarks</span></span>

<span data-ttu-id="7799c-109">L'uso dei metodi [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o i relativi equivalenti API sulla funzionalità specificata incrementa questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="7799c-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature increments this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7799c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7799c-110">Requirements</span></span>



| <span data-ttu-id="7799c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7799c-111">Requirement</span></span> | <span data-ttu-id="7799c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7799c-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7799c-113">Versione</span><span class="sxs-lookup"><span data-stu-id="7799c-113">Version</span></span><br/> | <span data-ttu-id="7799c-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7799c-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7799c-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7799c-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7799c-116">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="7799c-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7799c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7799c-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="7799c-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7799c-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7799c-119">IID</span><span class="sxs-lookup"><span data-stu-id="7799c-119">IID</span></span><br/>     | <span data-ttu-id="7799c-120">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7799c-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="7799c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7799c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7799c-122">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="7799c-122">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




