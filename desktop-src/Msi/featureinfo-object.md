---
description: L'oggetto FeatureInfo contiene informazioni relative alla funzionalità di destinazione e viene creato dall'oggetto Session usando il metodo FeatureInfo.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Oggetto FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324241"
---
# <a name="featureinfo-object"></a><span data-ttu-id="e55e5-103">Oggetto FeatureInfo</span><span class="sxs-lookup"><span data-stu-id="e55e5-103">FeatureInfo object</span></span>

<span data-ttu-id="e55e5-104">L'oggetto **FeatureInfo** contiene informazioni relative alla funzionalità di destinazione e viene creato dall'oggetto [**Session**](session-object.md) usando il metodo [**FeatureInfo**](session-featureinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e55e5-104">The **FeatureInfo** object contains information regarding the targeted feature and is created from the [**Session**](session-object.md) object using the [**FeatureInfo**](session-featureinfo.md) Method.</span></span>

## <a name="members"></a><span data-ttu-id="e55e5-105">Membri</span><span class="sxs-lookup"><span data-stu-id="e55e5-105">Members</span></span>

<span data-ttu-id="e55e5-106">L'oggetto **FeatureInfo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e55e5-106">The **FeatureInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="e55e5-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e55e5-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e55e5-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e55e5-108">Properties</span></span>

<span data-ttu-id="e55e5-109">L'oggetto **FeatureInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e55e5-109">The **FeatureInfo** object has these properties.</span></span>



| <span data-ttu-id="e55e5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e55e5-110">Property</span></span>                                                  | <span data-ttu-id="e55e5-111">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e55e5-111">Access type</span></span>           | <span data-ttu-id="e55e5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e55e5-112">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e55e5-113">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="e55e5-113">**Attributes**</span></span>](featureinfo-attributes.md)<br/>   | <span data-ttu-id="e55e5-114">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e55e5-114">Read/write</span></span><br/> | <span data-ttu-id="e55e5-115">Restituisce il valore per la funzionalità nella colonna Attributes della tabella Feature.</span><span class="sxs-lookup"><span data-stu-id="e55e5-115">Returns the value for the feature in the Attributes column of the Feature table.</span></span><br/> |
| [<span data-ttu-id="e55e5-116">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e55e5-116">**Description**</span></span>](featureinfo-description.md)<br/> |                       | <span data-ttu-id="e55e5-117">Restituisce la descrizione della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e55e5-117">Returns the description of the feature.</span></span><br/>                                          |
| [<span data-ttu-id="e55e5-118">**Titolo**</span><span class="sxs-lookup"><span data-stu-id="e55e5-118">**Title**</span></span>](featureinfo-title.md)<br/>             | <span data-ttu-id="e55e5-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="e55e5-119">Read-only</span></span><br/>  | <span data-ttu-id="e55e5-120">Restituisce il titolo della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e55e5-120">Returns the title of the feature.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="e55e5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e55e5-121">Requirements</span></span>



| <span data-ttu-id="e55e5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e55e5-122">Requirement</span></span> | <span data-ttu-id="e55e5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e55e5-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e55e5-124">Versione</span><span class="sxs-lookup"><span data-stu-id="e55e5-124">Version</span></span><br/> | <span data-ttu-id="e55e5-125">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e55e5-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e55e5-126">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e55e5-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e55e5-127">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e55e5-127">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e55e5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e55e5-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e55e5-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e55e5-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e55e5-130">IID</span><span class="sxs-lookup"><span data-stu-id="e55e5-130">IID</span></span><br/>     | <span data-ttu-id="e55e5-131">IID \_ IFeatureInfo è definito come 000C109F-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e55e5-131">IID\_IFeatureInfo is defined as 000C109F-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="e55e5-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e55e5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e55e5-133">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e55e5-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




