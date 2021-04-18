---
description: La proprietà FeatureState di sola lettura restituisce lo stato di installazione di una funzionalità.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Proprietà Installer. FeatureState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324635"
---
# <a name="installerfeaturestate-property"></a><span data-ttu-id="bb867-103">Proprietà Installer. FeatureState</span><span class="sxs-lookup"><span data-stu-id="bb867-103">Installer.FeatureState property</span></span>

<span data-ttu-id="bb867-104">La proprietà **FeatureState** di sola lettura restituisce lo stato di installazione di una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bb867-104">The read-only **FeatureState** property returns the installed state of a feature.</span></span>

<span data-ttu-id="bb867-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bb867-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb867-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb867-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a><span data-ttu-id="bb867-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bb867-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bb867-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb867-108">Remarks</span></span>

<span data-ttu-id="bb867-109">Questa proprietà restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb867-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="bb867-110">Valore</span><span class="sxs-lookup"><span data-stu-id="bb867-110">Value</span></span>                     | <span data-ttu-id="bb867-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb867-111">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="bb867-112">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="bb867-112">msiInstallStateAbsent</span></span>     | <span data-ttu-id="bb867-113">La funzionalità non è installata.</span><span class="sxs-lookup"><span data-stu-id="bb867-113">The feature is not installed.</span></span>                    |
| <span data-ttu-id="bb867-114">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="bb867-114">msiInstallStateAdvertised</span></span> | <span data-ttu-id="bb867-115">La funzionalità è annunciata.</span><span class="sxs-lookup"><span data-stu-id="bb867-115">The feature is advertised.</span></span>                       |
| <span data-ttu-id="bb867-116">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="bb867-116">msiInstallStateLocal</span></span>      | <span data-ttu-id="bb867-117">La funzionalità è installata per l'esecuzione in locale.</span><span class="sxs-lookup"><span data-stu-id="bb867-117">The feature is installed to run locally.</span></span>         |
| <span data-ttu-id="bb867-118">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="bb867-118">msiInstallStateSource</span></span>     | <span data-ttu-id="bb867-119">La funzionalità è installata per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="bb867-119">The feature is installed to run from source.</span></span>     |
| <span data-ttu-id="bb867-120">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="bb867-120">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="bb867-121">Un parametro non valido è stato passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="bb867-121">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="bb867-122">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="bb867-122">msiInstallStateUnknown</span></span>    | <span data-ttu-id="bb867-123">Il codice prodotto o l'ID funzionalità è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bb867-123">The product code or feature ID is unknown.</span></span>       |
| <span data-ttu-id="bb867-124">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="bb867-124">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="bb867-125">I dati di configurazione sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="bb867-125">The configuration data is corrupt.</span></span>               |



 

 

<span data-ttu-id="bb867-126">La proprietà **FeatureState** non verifica che la funzionalità sia accessibile.</span><span class="sxs-lookup"><span data-stu-id="bb867-126">The **FeatureState** property does not validate that the feature is accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb867-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb867-127">Requirements</span></span>



| <span data-ttu-id="bb867-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb867-128">Requirement</span></span> | <span data-ttu-id="bb867-129">Valore</span><span class="sxs-lookup"><span data-stu-id="bb867-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb867-130">Versione</span><span class="sxs-lookup"><span data-stu-id="bb867-130">Version</span></span><br/> | <span data-ttu-id="bb867-131">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb867-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bb867-132">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bb867-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bb867-133">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb867-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bb867-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bb867-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="bb867-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb867-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bb867-136">IID</span><span class="sxs-lookup"><span data-stu-id="bb867-136">IID</span></span><br/>     | <span data-ttu-id="bb867-137">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bb867-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="bb867-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb867-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb867-139">**MsiQueryFeatureState**</span><span class="sxs-lookup"><span data-stu-id="bb867-139">**MsiQueryFeatureState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




