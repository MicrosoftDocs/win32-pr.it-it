---
title: Interfaccia IWMPError (VB e C) (WMP. h)
description: Fornisce proprietà e metodi per l'accesso a una raccolta di interfacce IWMPErrorItem per il recupero di informazioni sugli errori. L'interfaccia IWMPError espone le proprietà seguenti.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- Interfaccia IWMPError (VB e C) Windows Media Player
- Interfaccia IWMPError (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPError (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289a39093c38e7a4b0cc43cb8f318e321ae8ef53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328207"
---
# <a name="iwmperror-vb-and-c-interface"></a><span data-ttu-id="22079-105">Interfaccia IWMPError (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="22079-105">IWMPError (VB and C#) interface</span></span>

<span data-ttu-id="22079-106">Fornisce proprietà e metodi per l'accesso a una raccolta di interfacce **IWMPErrorItem** per il recupero di informazioni sugli errori.</span><span class="sxs-lookup"><span data-stu-id="22079-106">Provides properties and methods for accessing a collection of **IWMPErrorItem** interfaces for retrieving error information.</span></span>

<span data-ttu-id="22079-107">L'interfaccia **IWMPError** espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="22079-107">The **IWMPError** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="22079-108">Membri</span><span class="sxs-lookup"><span data-stu-id="22079-108">Members</span></span>

<span data-ttu-id="22079-109">L'interfaccia **IWMPError (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="22079-109">The **IWMPError (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="22079-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="22079-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="22079-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22079-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22079-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="22079-112">Methods</span></span>

<span data-ttu-id="22079-113">L'interfaccia **IWMPError (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="22079-113">The **IWMPError (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="22079-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="22079-114">Method</span></span>                                                                         | <span data-ttu-id="22079-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22079-115">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22079-116">**clearErrorQueue**</span><span class="sxs-lookup"><span data-stu-id="22079-116">**clearErrorQueue**</span></span>](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | <span data-ttu-id="22079-117">Cancella gli errori dalla coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="22079-117">Clears the errors from the error queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="22079-118">**webHelp**</span><span class="sxs-lookup"><span data-stu-id="22079-118">**webHelp**</span></span>](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | <span data-ttu-id="22079-119">Avvia la pagina della guida del Web Microsoft Windows Media Player per visualizzare ulteriori informazioni sul primo errore nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="22079-119">Launches the Microsoft Windows Media Player Web Help page to display further information about the first error in the error queue.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="22079-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22079-120">Properties</span></span>

<span data-ttu-id="22079-121">L'interfaccia **IWMPError (VB e C#)** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="22079-121">The **IWMPError (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="22079-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22079-122">Property</span></span>                                                                        | <span data-ttu-id="22079-123">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="22079-123">Access type</span></span>           | <span data-ttu-id="22079-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22079-124">Description</span></span>                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22079-125">**errorCount**</span><span class="sxs-lookup"><span data-stu-id="22079-125">**errorCount**</span></span>](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | <span data-ttu-id="22079-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="22079-126">Read-only</span></span><br/>  | <span data-ttu-id="22079-127">Ottiene il numero di errori nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="22079-127">Gets the number of errors in the error queue.</span></span><br/>                                                                            |
| [<span data-ttu-id="22079-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="22079-128">**Item**</span></span>](iwmperror-item--vb-and-c.md)<br/>                             | <span data-ttu-id="22079-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="22079-129">Read/write</span></span><br/> | <span data-ttu-id="22079-130">Ottiene un'interfaccia **IWMPErrorItem** in corrispondenza dell'indice specificato nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="22079-130">Gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span> <span data-ttu-id="22079-131">In C# si tratta del metodo **get \_ Item** .</span><span class="sxs-lookup"><span data-stu-id="22079-131">In C#, this is the **get\_Item** method.</span></span><br/> |



 

<span data-ttu-id="22079-132">Ottenere un'interfaccia **IWMPError** usando la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="22079-132">Get an **IWMPError** interface by using the following property.</span></span>



| <span data-ttu-id="22079-133">Oggetto</span><span class="sxs-lookup"><span data-stu-id="22079-133">Object</span></span>                                                                   | <span data-ttu-id="22079-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22079-134">Property</span></span>                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="22079-135">Oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="22079-135">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="22079-136">**Errore**</span><span class="sxs-lookup"><span data-stu-id="22079-136">**Error**</span></span>](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="22079-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22079-137">Requirements</span></span>



| <span data-ttu-id="22079-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="22079-138">Requirement</span></span> | <span data-ttu-id="22079-139">Valore</span><span class="sxs-lookup"><span data-stu-id="22079-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="22079-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22079-140">Header</span></span><br/> | <dl> <span data-ttu-id="22079-141"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="22079-141"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22079-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22079-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22079-143">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="22079-143">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="22079-144">**Interfaccia IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="22079-144">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





