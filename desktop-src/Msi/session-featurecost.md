---
description: La proprietà FeatureCost dell'oggetto Session restituisce la quantità totale di spazio su disco, in unità di 512 byte, richiesta dalla funzionalità specificata e dalle relative funzionalità padre (fino alla radice della tabella delle funzionalità).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Proprietà Session. FeatureCost
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329106"
---
# <a name="sessionfeaturecost-property"></a><span data-ttu-id="274d7-103">Proprietà Session. FeatureCost</span><span class="sxs-lookup"><span data-stu-id="274d7-103">Session.FeatureCost property</span></span>

<span data-ttu-id="274d7-104">La proprietà **FeatureCost** dell'oggetto [**Session**](session-object.md) restituisce la quantità totale di spazio su disco, in unità di 512 byte, richiesta dalla funzionalità specificata e dalle relative funzionalità padre (fino alla radice della tabella delle funzionalità).</span><span class="sxs-lookup"><span data-stu-id="274d7-104">The **FeatureCost** property of the [**Session**](session-object.md) object returns the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the Feature table).</span></span> <span data-ttu-id="274d7-105">Per ogni funzionalità, il costo totale è costituito dai costi del disco attribuiti a ogni componente collegato alla funzionalità.</span><span class="sxs-lookup"><span data-stu-id="274d7-105">For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.</span></span>

<span data-ttu-id="274d7-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="274d7-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="274d7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="274d7-107">Syntax</span></span>


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a><span data-ttu-id="274d7-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="274d7-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="274d7-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="274d7-109">Remarks</span></span>

<span data-ttu-id="274d7-110">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="274d7-110">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="274d7-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="274d7-111">Requirements</span></span>



| <span data-ttu-id="274d7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="274d7-112">Requirement</span></span> | <span data-ttu-id="274d7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="274d7-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="274d7-114">Versione</span><span class="sxs-lookup"><span data-stu-id="274d7-114">Version</span></span><br/> | <span data-ttu-id="274d7-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="274d7-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="274d7-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="274d7-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="274d7-117">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="274d7-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="274d7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="274d7-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="274d7-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="274d7-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="274d7-120">IID</span><span class="sxs-lookup"><span data-stu-id="274d7-120">IID</span></span><br/>     | <span data-ttu-id="274d7-121">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="274d7-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




