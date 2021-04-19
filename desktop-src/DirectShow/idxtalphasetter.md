---
description: L'interfaccia IDxtAlphaSetter imposta le proprietà sull'effetto Setter alfa. Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando viene eseguito il rendering dell'effetto Alpha Setter.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interfaccia IDxtAlphaSetter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330175"
---
# <a name="idxtalphasetter-interface"></a><span data-ttu-id="25ef4-103">Interfaccia IDxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="25ef4-103">IDxtAlphaSetter interface</span></span>

> [!Note]  
> <span data-ttu-id="25ef4-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="25ef4-104">\[Deprecated.</span></span> <span data-ttu-id="25ef4-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="25ef4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="25ef4-106">L' `IDxtAlphaSetter` interfaccia imposta le proprietà sull'effetto del [Setter alfa](alpha-setter-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="25ef4-106">The `IDxtAlphaSetter` interface sets properties on the [Alpha Setter](alpha-setter-effect.md) effect.</span></span>

<span data-ttu-id="25ef4-107">Questa interfaccia viene utilizzata internamente da DirectShow editing Services (DES) quando viene eseguito il rendering dell'effetto Alpha Setter.</span><span class="sxs-lookup"><span data-stu-id="25ef4-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Alpha Setter effect.</span></span> <span data-ttu-id="25ef4-108">Non è necessario che le applicazioni DES usino questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="25ef4-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="25ef4-109">Per impostare le proprietà di una transizione in DES, utilizzare l'interfaccia [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="25ef4-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="25ef4-110">Membri</span><span class="sxs-lookup"><span data-stu-id="25ef4-110">Members</span></span>

<span data-ttu-id="25ef4-111">L'interfaccia **IDxtAlphaSetter** eredita da **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="25ef4-111">The **IDxtAlphaSetter** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="25ef4-112">**IDxtAlphaSetter** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="25ef4-112">**IDxtAlphaSetter** also has these types of members:</span></span>

-   [<span data-ttu-id="25ef4-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="25ef4-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="25ef4-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="25ef4-114">Methods</span></span>

<span data-ttu-id="25ef4-115">L'interfaccia **IDxtAlphaSetter** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="25ef4-115">The **IDxtAlphaSetter** interface has these methods.</span></span>



| <span data-ttu-id="25ef4-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="25ef4-116">Method</span></span>                                                  | <span data-ttu-id="25ef4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25ef4-117">Description</span></span>                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="25ef4-118">**Ottieni \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="25ef4-118">**get\_Alpha**</span></span>](idxtalphasetter-get-alpha.md)         | <span data-ttu-id="25ef4-119">Recupera il valore alfa per l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="25ef4-119">Retrieves the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="25ef4-120">**ottenere \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="25ef4-120">**get\_AlphaRamp**</span></span>](idxtalphasetter-get-alpharamp.md) | <span data-ttu-id="25ef4-121">Recupera la proprietà della rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="25ef4-121">Retrieves the alpha ramp property.</span></span><br/>              |
| [<span data-ttu-id="25ef4-122">**Inserisci \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="25ef4-122">**put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)         | <span data-ttu-id="25ef4-123">Specifica il valore alfa per l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="25ef4-123">Specifies the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="25ef4-124">**Inserisci \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="25ef4-124">**put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md) | <span data-ttu-id="25ef4-125">Specifica la proprietà della rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="25ef4-125">Specifies the alpha ramp property.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="25ef4-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="25ef4-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="25ef4-127">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="25ef4-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="25ef4-128">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="25ef4-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="25ef4-129">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="25ef4-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25ef4-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25ef4-130">Requirements</span></span>



| <span data-ttu-id="25ef4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="25ef4-131">Requirement</span></span> | <span data-ttu-id="25ef4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="25ef4-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25ef4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25ef4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="25ef4-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ef4-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="25ef4-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="25ef4-135">Library</span></span><br/> | <dl> <span data-ttu-id="25ef4-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25ef4-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




