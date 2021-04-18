---
description: L'interfaccia IDxtKey imposta le proprietà per la transizione della chiave. Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione della chiave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interfaccia IDxtKey (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328611"
---
# <a name="idxtkey-interface"></a><span data-ttu-id="b7e1a-103">Interfaccia IDxtKey</span><span class="sxs-lookup"><span data-stu-id="b7e1a-103">IDxtKey interface</span></span>

> [!Note]  
> <span data-ttu-id="b7e1a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-104">\[Deprecated.</span></span> <span data-ttu-id="b7e1a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b7e1a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b7e1a-106">L' `IDxtKey` interfaccia imposta le proprietà della transizione della [chiave](key-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="b7e1a-106">The `IDxtKey` interface sets properties on the [Key](key-transition.md) transition.</span></span>

<span data-ttu-id="b7e1a-107">Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando esegue il rendering della transizione della chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Key transition.</span></span> <span data-ttu-id="b7e1a-108">Non è necessario che le applicazioni DES usino questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="b7e1a-109">Per impostare le proprietà di una transizione in DES, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="b7e1a-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="b7e1a-110">Membri</span><span class="sxs-lookup"><span data-stu-id="b7e1a-110">Members</span></span>

<span data-ttu-id="b7e1a-111">L'interfaccia **IDxtKey** eredita da **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-111">The **IDxtKey** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="b7e1a-112">**IDxtKey** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b7e1a-112">**IDxtKey** also has these types of members:</span></span>

-   [<span data-ttu-id="b7e1a-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b7e1a-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b7e1a-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b7e1a-114">Methods</span></span>

<span data-ttu-id="b7e1a-115">L'interfaccia **IDxtKey** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-115">The **IDxtKey** interface has these methods.</span></span>



| <span data-ttu-id="b7e1a-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="b7e1a-116">Method</span></span>                                            | <span data-ttu-id="b7e1a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7e1a-117">Description</span></span>                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7e1a-118">**ottenere \_ Hue**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-118">**get\_Hue**</span></span>](idxtkey-get-hue.md)               | <span data-ttu-id="b7e1a-119">Recupera il valore di tonalità su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-119">Retrieves the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="b7e1a-120">**Ottieni \_ Inverti**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-120">**get\_Invert**</span></span>](idxtkey-get-invert.md)         | <span data-ttu-id="b7e1a-121">Recupera un valore booleano che indica se l'operazione del tasto è invertita.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-121">Retrieves a Boolean value indicating whether the key operation is inverted.</span></span><br/> |
| [<span data-ttu-id="b7e1a-122">**ottenere il \_ tipo di**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-122">**get\_KeyType**</span></span>](idxtkey-get-keytype.md)       | <span data-ttu-id="b7e1a-123">Recupera il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-123">Retrieves the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="b7e1a-124">**Ottieni \_ luminanza**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-124">**get\_Luminance**</span></span>](idxtkey-get-luminance.md)   | <span data-ttu-id="b7e1a-125">Recupera il valore di luminanza su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-125">Retrieves the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="b7e1a-126">**Ottieni \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-126">**get\_RGB**</span></span>](idxtkey-get-rgb.md)               | <span data-ttu-id="b7e1a-127">Recupera il colore RGB su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-127">Retrieves the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="b7e1a-128">**Ottieni \_ somiglianza**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-128">**get\_Similarity**</span></span>](idxtkey-get-similarity.md) | <span data-ttu-id="b7e1a-129">Recupera l'intervallo di dati del colore che diventa trasparente.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-129">Retrieves the range of color data that becomes transparent.</span></span><br/>                 |
| [<span data-ttu-id="b7e1a-130">**Inserisci \_ tonalità**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-130">**put\_Hue**</span></span>](idxtkey-put-hue.md)               | <span data-ttu-id="b7e1a-131">Specifica il valore di tonalità su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-131">Specifies the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="b7e1a-132">**Inserisci \_ Inverti**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-132">**put\_Invert**</span></span>](idxtkey-put-invert.md)         | <span data-ttu-id="b7e1a-133">Specifica se l'operazione chiave è invertita.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-133">Specifies whether the key operation is inverted.</span></span><br/>                            |
| [<span data-ttu-id="b7e1a-134">**Inserisci \_ tipo di tipo**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-134">**put\_KeyType**</span></span>](idxtkey-put-keytype.md)       | <span data-ttu-id="b7e1a-135">Specifica il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-135">Specifies the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="b7e1a-136">**\_luminanza put**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-136">**put\_Luminance**</span></span>](idxtkey-put-luminance.md)   | <span data-ttu-id="b7e1a-137">Specifica il valore di luminanza su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-137">Specifies the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="b7e1a-138">**Inserisci \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-138">**put\_RGB**</span></span>](idxtkey-put-rgb.md)               | <span data-ttu-id="b7e1a-139">Specifica il colore RGB su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-139">Specifies the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="b7e1a-140">**Inserisci \_ somiglianza**</span><span class="sxs-lookup"><span data-stu-id="b7e1a-140">**put\_Similarity**</span></span>](idxtkey-put-similarity.md) | <span data-ttu-id="b7e1a-141">Specifica l'intervallo di dati del colore che diventa trasparente.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-141">Specifies the range of color data that becomes transparent.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="b7e1a-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7e1a-142">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7e1a-143">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-143">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b7e1a-144">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b7e1a-144">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b7e1a-145">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b7e1a-145">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7e1a-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7e1a-146">Requirements</span></span>



| <span data-ttu-id="b7e1a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e1a-147">Requirement</span></span> | <span data-ttu-id="b7e1a-148">Valore</span><span class="sxs-lookup"><span data-stu-id="b7e1a-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e1a-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7e1a-149">Header</span></span><br/>  | <dl> <span data-ttu-id="b7e1a-150"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1a-150"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b7e1a-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7e1a-151">Library</span></span><br/> | <dl> <span data-ttu-id="b7e1a-152"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7e1a-152"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




