---
description: Il metodo UseFeature dell'oggetto Installer incrementa il conteggio di utilizzo per una particolare funzionalità e restituisce lo stato di installazione per tale funzionalità. Questo metodo deve essere usato per indicare l'intenzione di un'applicazione di usare una funzionalità.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Installer. UseFeature, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332164"
---
# <a name="installerusefeature-method"></a><span data-ttu-id="200d1-104">Installer. UseFeature, metodo</span><span class="sxs-lookup"><span data-stu-id="200d1-104">Installer.UseFeature method</span></span>

<span data-ttu-id="200d1-105">Il metodo **UseFeature** dell'oggetto [**Installer**](installer-object.md) incrementa il conteggio di utilizzo per una particolare funzionalità e restituisce lo stato di installazione per tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="200d1-105">The **UseFeature** method of the [**Installer**](installer-object.md) object increments the usage count for a particular feature and returns the installation state for that feature.</span></span> <span data-ttu-id="200d1-106">Questo metodo deve essere usato per indicare l'intenzione di un'applicazione di usare una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="200d1-106">This method should be used to indicate an application's intent to use a feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="200d1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="200d1-107">Syntax</span></span>


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="200d1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="200d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="200d1-109">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="200d1-109">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="200d1-110">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="200d1-110">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="200d1-111">*Funzionalità*</span><span class="sxs-lookup"><span data-stu-id="200d1-111">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="200d1-112">Identifica la funzionalità da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="200d1-112">Identifies the feature to be used.</span></span>

</dd> <dt>

<span data-ttu-id="200d1-113">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="200d1-113">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="200d1-114">Questo parametro deve essere *msiInstallModeNoDetection*.</span><span class="sxs-lookup"><span data-stu-id="200d1-114">This parameter must be *msiInstallModeNoDetection*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="200d1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="200d1-115">Return value</span></span>

<span data-ttu-id="200d1-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="200d1-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="200d1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="200d1-117">Remarks</span></span>

<span data-ttu-id="200d1-118">Il metodo **UseFeature** deve essere usato solo su funzionalità note per la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="200d1-118">The **UseFeature** method should only be used on features known to be published.</span></span> <span data-ttu-id="200d1-119">L'applicazione deve determinare lo stato della funzionalità chiamando la proprietà [**FeatureState**](installer-featurestate.md) o la proprietà [**features**](installer-features.md) o i rispettivi equivalenti API.</span><span class="sxs-lookup"><span data-stu-id="200d1-119">The application should determine the status of the feature by calling either the [**FeatureState**](installer-featurestate.md) property or [**Features**](installer-features.md) property or their API equivalents.</span></span>

## <a name="requirements"></a><span data-ttu-id="200d1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="200d1-120">Requirements</span></span>



| <span data-ttu-id="200d1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="200d1-121">Requirement</span></span> | <span data-ttu-id="200d1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="200d1-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200d1-123">Versione</span><span class="sxs-lookup"><span data-stu-id="200d1-123">Version</span></span><br/> | <span data-ttu-id="200d1-124">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="200d1-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="200d1-125">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="200d1-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="200d1-126">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="200d1-126">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="200d1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="200d1-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="200d1-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="200d1-128"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="200d1-129">IID</span><span class="sxs-lookup"><span data-stu-id="200d1-129">IID</span></span><br/>     | <span data-ttu-id="200d1-130">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="200d1-130">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="200d1-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="200d1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200d1-132">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="200d1-132">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




