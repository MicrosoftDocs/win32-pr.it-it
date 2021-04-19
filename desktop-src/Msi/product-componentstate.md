---
description: La proprietà ComponentState è lo stato di installazione del componente per l'istanza di questo prodotto. Questa proprietà chiama MsiQueryComponentState con ProductCode, UserSid e Context dell'oggetto.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Metodo Product. ComponentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330283"
---
# <a name="productcomponentstate-method"></a><span data-ttu-id="bd56c-103">Metodo Product. ComponentState</span><span class="sxs-lookup"><span data-stu-id="bd56c-103">Product.ComponentState method</span></span>

<span data-ttu-id="bd56c-104">La proprietà **ComponentState** è lo stato di installazione del componente per l'istanza di questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="bd56c-104">The **ComponentState** property is the installation state of the component for the instance of this product.</span></span>

<span data-ttu-id="bd56c-105">Questa proprietà chiama [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)con ProductCode, UserSID e Context dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bd56c-105">This property calls [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), with the ProductCode, UserSid, and Context of the object.</span></span> <span data-ttu-id="bd56c-106">Il GUID dell'ID componente viene fornito come parametro.</span><span class="sxs-lookup"><span data-stu-id="bd56c-106">The component Id GUID is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd56c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd56c-107">Syntax</span></span>


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a><span data-ttu-id="bd56c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd56c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd56c-109">*ID*</span><span class="sxs-lookup"><span data-stu-id="bd56c-109">*ID*</span></span> 
</dt> <dd>

<span data-ttu-id="bd56c-110">GUID del codice componente del componente, disponibile nella colonna ComponentID della tabella dei [componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="bd56c-110">Component code GUID of the component as found in the ComponentID column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd56c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd56c-111">Return value</span></span>

<span data-ttu-id="bd56c-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bd56c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd56c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd56c-113">Remarks</span></span>

<span data-ttu-id="bd56c-114">Se la chiamata ha esito positivo, la proprietà contiene il valore come **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="bd56c-114">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="bd56c-115">State</span><span class="sxs-lookup"><span data-stu-id="bd56c-115">State</span></span>                | <span data-ttu-id="bd56c-116">Significato</span><span class="sxs-lookup"><span data-stu-id="bd56c-116">Meaning</span></span>                                            |
|----------------------|----------------------------------------------------|
| <span data-ttu-id="bd56c-117">INSTALLSTATE \_ locale</span><span class="sxs-lookup"><span data-stu-id="bd56c-117">INSTALLSTATE\_LOCAL</span></span>  | <span data-ttu-id="bd56c-118">Il componente viene installato localmente.</span><span class="sxs-lookup"><span data-stu-id="bd56c-118">The component is installed locally.</span></span>                |
| <span data-ttu-id="bd56c-119">\_origine InstallState</span><span class="sxs-lookup"><span data-stu-id="bd56c-119">INSTALLSTATE\_SOURCE</span></span> | <span data-ttu-id="bd56c-120">Il componente è installato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="bd56c-120">The component is installed to run from the source.</span></span> |



 

<span data-ttu-id="bd56c-121">Se la chiamata ha esito negativo, la proprietà contiene un codice di errore di [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span><span class="sxs-lookup"><span data-stu-id="bd56c-121">If the call fails, the property contains an error code from [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span></span>



| <span data-ttu-id="bd56c-122">Errore</span><span class="sxs-lookup"><span data-stu-id="bd56c-122">Error</span></span>                     | <span data-ttu-id="bd56c-123">Significato</span><span class="sxs-lookup"><span data-stu-id="bd56c-123">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd56c-124">ERRORE di \_ accesso \_ negato</span><span class="sxs-lookup"><span data-stu-id="bd56c-124">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="bd56c-125">Il processo chiamante deve disporre di privilegi amministrativi per ottenere informazioni per un utente diverso dall'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="bd56c-125">The calling process must have administrative privileges to get information for a user other than the current user.</span></span> |
| <span data-ttu-id="bd56c-126">ERRORE \_ configurazione errata \_</span><span class="sxs-lookup"><span data-stu-id="bd56c-126">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="bd56c-127">I dati di configurazione sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="bd56c-127">The configuration data is corrupt.</span></span>                                                                                 |
| <span data-ttu-id="bd56c-128">ERRORE \_ parametro non valido \_</span><span class="sxs-lookup"><span data-stu-id="bd56c-128">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="bd56c-129">Un parametro non valido è stato passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="bd56c-129">An invalid parameter was passed to the function.</span></span>                                                                   |
| <span data-ttu-id="bd56c-130">ERRORE \_ riuscito</span><span class="sxs-lookup"><span data-stu-id="bd56c-130">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="bd56c-131">La funzione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bd56c-131">The function completed successfully.</span></span>                                                                               |
| <span data-ttu-id="bd56c-132">ERRORE \_ \_ componente sconosciuto</span><span class="sxs-lookup"><span data-stu-id="bd56c-132">ERROR\_UNKNOWN\_COMPONENT</span></span> | <span data-ttu-id="bd56c-133">L'ID componente non identifica un componente noto.</span><span class="sxs-lookup"><span data-stu-id="bd56c-133">The component ID does not identify a known component.</span></span>                                                              |
| <span data-ttu-id="bd56c-134">ERRORE \_ \_ prodotto sconosciuto</span><span class="sxs-lookup"><span data-stu-id="bd56c-134">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="bd56c-135">Il codice prodotto non identifica un prodotto noto.</span><span class="sxs-lookup"><span data-stu-id="bd56c-135">The product code does not identify a known product.</span></span>                                                                |
| <span data-ttu-id="bd56c-136">\_funzione Error \_ non riuscita</span><span class="sxs-lookup"><span data-stu-id="bd56c-136">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="bd56c-137">Errore interno imprevisto.</span><span class="sxs-lookup"><span data-stu-id="bd56c-137">An unexpected internal failure.</span></span>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="bd56c-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd56c-138">Requirements</span></span>



| <span data-ttu-id="bd56c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd56c-139">Requirement</span></span> | <span data-ttu-id="bd56c-140">Valore</span><span class="sxs-lookup"><span data-stu-id="bd56c-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd56c-141">Versione</span><span class="sxs-lookup"><span data-stu-id="bd56c-141">Version</span></span><br/> | <span data-ttu-id="bd56c-142">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bd56c-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bd56c-143">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bd56c-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bd56c-144">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bd56c-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="bd56c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bd56c-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="bd56c-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd56c-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="bd56c-147">IID</span><span class="sxs-lookup"><span data-stu-id="bd56c-147">IID</span></span><br/>     | <span data-ttu-id="bd56c-148">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bd56c-148">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="bd56c-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd56c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd56c-150">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="bd56c-150">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="bd56c-151">**MsiQueryComponentState**</span><span class="sxs-lookup"><span data-stu-id="bd56c-151">**MsiQueryComponentState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[<span data-ttu-id="bd56c-152">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="bd56c-152">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




