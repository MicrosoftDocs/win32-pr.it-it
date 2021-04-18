---
description: La proprietà FeatureState è lo stato di installazione della funzionalità per l'istanza di questo prodotto. Questa proprietà chiama MsiQueryFeatureStateEx con ProductCode, UserSid e Context dell'oggetto. L'ID funzionalità viene fornito come parametro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Metodo Product. FeatureState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326984"
---
# <a name="productfeaturestate-method"></a><span data-ttu-id="a9f73-104">Metodo Product. FeatureState</span><span class="sxs-lookup"><span data-stu-id="a9f73-104">Product.FeatureState method</span></span>

<span data-ttu-id="a9f73-105">La proprietà **FeatureState** è lo stato di installazione della funzionalità per l'istanza di questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="a9f73-105">The **FeatureState** property is the installation state of the feature for the instance of this product.</span></span>

<span data-ttu-id="a9f73-106">Questa proprietà chiama [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)con *ProductCode*, *UserSID* e *context* dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9f73-106">This property calls [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), with the *ProductCode*, *UserSid* and *Context* of the object.</span></span> <span data-ttu-id="a9f73-107">L'ID funzionalità viene fornito come parametro.</span><span class="sxs-lookup"><span data-stu-id="a9f73-107">The feature Id is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f73-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9f73-108">Syntax</span></span>


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a><span data-ttu-id="a9f73-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9f73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9f73-110">*FeatureId*</span><span class="sxs-lookup"><span data-stu-id="a9f73-110">*FeatureId*</span></span> 
</dt> <dd>

<span data-ttu-id="a9f73-111">ID funzionalità visualizzato nella colonna funzionalità della [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="a9f73-111">Feature Id appearing in the Feature column of the [Feature Table](feature-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9f73-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9f73-112">Return value</span></span>

<span data-ttu-id="a9f73-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a9f73-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9f73-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9f73-114">Remarks</span></span>

<span data-ttu-id="a9f73-115">Se la chiamata ha esito positivo, la proprietà contiene il valore come **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="a9f73-115">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="a9f73-116">State</span><span class="sxs-lookup"><span data-stu-id="a9f73-116">State</span></span>                    | <span data-ttu-id="a9f73-117">Significato</span><span class="sxs-lookup"><span data-stu-id="a9f73-117">Meaning</span></span>                                      |
|--------------------------|----------------------------------------------|
| <span data-ttu-id="a9f73-118">INSTALLSTATE \_ annunciata</span><span class="sxs-lookup"><span data-stu-id="a9f73-118">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="a9f73-119">Questa funzionalità è annunciata.</span><span class="sxs-lookup"><span data-stu-id="a9f73-119">This feature is advertised.</span></span>                  |
| <span data-ttu-id="a9f73-120">INSTALLSTATE \_ locale</span><span class="sxs-lookup"><span data-stu-id="a9f73-120">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="a9f73-121">La funzionalità viene installata localmente.</span><span class="sxs-lookup"><span data-stu-id="a9f73-121">The feature is installed locally.</span></span>            |
| <span data-ttu-id="a9f73-122">\_origine InstallState</span><span class="sxs-lookup"><span data-stu-id="a9f73-122">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="a9f73-123">La funzionalità è installata per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a9f73-123">The feature is installed to run from source.</span></span> |



 

<span data-ttu-id="a9f73-124">Se la chiamata ha esito negativo, la proprietà contiene un codice di errore di [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span><span class="sxs-lookup"><span data-stu-id="a9f73-124">If the call fails, the property contains an error code from [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span></span>



| <span data-ttu-id="a9f73-125">Errore</span><span class="sxs-lookup"><span data-stu-id="a9f73-125">Error</span></span>                     | <span data-ttu-id="a9f73-126">Significato</span><span class="sxs-lookup"><span data-stu-id="a9f73-126">Meaning</span></span>                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f73-127">ERRORE di \_ accesso \_ negato</span><span class="sxs-lookup"><span data-stu-id="a9f73-127">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="a9f73-128">Il processo chiamante deve disporre di privilegi amministrativi per ottenere informazioni relative a un prodotto installato per un utente diverso dall'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a9f73-128">The calling process must have administrative privileges to get information for a product installed for a user other than the current user.</span></span> |
| <span data-ttu-id="a9f73-129">ERRORE \_ configurazione errata \_</span><span class="sxs-lookup"><span data-stu-id="a9f73-129">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="a9f73-130">I dati di configurazione sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="a9f73-130">The configuration data is corrupt.</span></span>                                                                                                         |
| <span data-ttu-id="a9f73-131">ERRORE \_ parametro non valido \_</span><span class="sxs-lookup"><span data-stu-id="a9f73-131">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="a9f73-132">Un parametro non valido è stato passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="a9f73-132">An invalid parameter was passed to the function.</span></span>                                                                                           |
| <span data-ttu-id="a9f73-133">ERRORE \_ riuscito</span><span class="sxs-lookup"><span data-stu-id="a9f73-133">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="a9f73-134">La funzione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a9f73-134">The function completed successfully.</span></span>                                                                                                       |
| <span data-ttu-id="a9f73-135">\_funzionalità sconosciuta di errore \_</span><span class="sxs-lookup"><span data-stu-id="a9f73-135">ERROR\_UNKNOWN\_FEATURE</span></span>   | <span data-ttu-id="a9f73-136">L'ID funzionalità non identifica una funzionalità nota.</span><span class="sxs-lookup"><span data-stu-id="a9f73-136">The feature ID does not identify a known feature.</span></span>                                                                                          |
| <span data-ttu-id="a9f73-137">ERRORE \_ \_ prodotto sconosciuto</span><span class="sxs-lookup"><span data-stu-id="a9f73-137">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="a9f73-138">Il codice prodotto non identifica un prodotto noto.</span><span class="sxs-lookup"><span data-stu-id="a9f73-138">The product code does not identify a known product.</span></span>                                                                                        |
| <span data-ttu-id="a9f73-139">\_funzione Error \_ non riuscita</span><span class="sxs-lookup"><span data-stu-id="a9f73-139">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="a9f73-140">Errore interno imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a9f73-140">An unexpected internal failure.</span></span>                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="a9f73-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9f73-141">Requirements</span></span>



| <span data-ttu-id="a9f73-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9f73-142">Requirement</span></span> | <span data-ttu-id="a9f73-143">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f73-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f73-144">Versione</span><span class="sxs-lookup"><span data-stu-id="a9f73-144">Version</span></span><br/> | <span data-ttu-id="a9f73-145">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a9f73-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a9f73-146">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a9f73-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a9f73-147">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a9f73-147">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a9f73-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a9f73-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="a9f73-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9f73-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a9f73-150">IID</span><span class="sxs-lookup"><span data-stu-id="a9f73-150">IID</span></span><br/>     | <span data-ttu-id="a9f73-151">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a9f73-151">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="a9f73-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9f73-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f73-153">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="a9f73-153">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="a9f73-154">**MsiQueryFeatureStateEx**</span><span class="sxs-lookup"><span data-stu-id="a9f73-154">**MsiQueryFeatureStateEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[<span data-ttu-id="a9f73-155">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="a9f73-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




