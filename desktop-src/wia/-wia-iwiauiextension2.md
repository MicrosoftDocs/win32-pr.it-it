---
description: L'interfaccia IWiaUIExtension2 fornisce metodi che sostituiscono l'interfaccia utente predefinita fornita dal sistema con un'interfaccia utente personalizzata e che forniscono un'icona di dispositivo personalizzata.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interfaccia IWiaUIExtension2 (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966721"
---
# <a name="iwiauiextension2-interface"></a><span data-ttu-id="f457a-103">Interfaccia IWiaUIExtension2</span><span class="sxs-lookup"><span data-stu-id="f457a-103">IWiaUIExtension2 interface</span></span>

<span data-ttu-id="f457a-104">L'interfaccia IWiaUIExtension2 fornisce metodi che sostituiscono l'interfaccia utente predefinita fornita dal sistema con un'interfaccia utente personalizzata e che forniscono un'icona di dispositivo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f457a-104">The IWiaUIExtension2 interface provides methods that replace the default, system-supplied user interface with a custom user interface, and that provide a custom device icon.</span></span> <span data-ttu-id="f457a-105">I fornitori di dispositivi possono implementare questa interfaccia per fornire interfacce utente personalizzate per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f457a-105">Device vendors can implement this interface to provide custom user interfaces for their devices.</span></span>

## <a name="members"></a><span data-ttu-id="f457a-106">Membri</span><span class="sxs-lookup"><span data-stu-id="f457a-106">Members</span></span>

<span data-ttu-id="f457a-107">L'interfaccia **IWiaUIExtension2** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f457a-107">The **IWiaUIExtension2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f457a-108">**IWiaUIExtension2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f457a-108">**IWiaUIExtension2** also has these types of members:</span></span>

-   [<span data-ttu-id="f457a-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f457a-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f457a-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="f457a-110">Methods</span></span>

<span data-ttu-id="f457a-111">L'interfaccia **IWiaUIExtension2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f457a-111">The **IWiaUIExtension2** interface has these methods.</span></span>



| <span data-ttu-id="f457a-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="f457a-112">Method</span></span>                                                       | <span data-ttu-id="f457a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f457a-113">Description</span></span>                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f457a-114">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="f457a-114">**DeviceDialog**</span></span>](-wia-iwiauiextension2-devicedialog.md)   | <span data-ttu-id="f457a-115">Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="f457a-115">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="f457a-116">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="f457a-116">**GetDeviceIcon**</span></span>](-wia-iwiauiextension2-getdeviceicon.md) | <span data-ttu-id="f457a-117">Ottiene un'icona di dispositivo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f457a-117">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="f457a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f457a-118">Remarks</span></span>



| <span data-ttu-id="f457a-119">Metodi IUnknown</span><span class="sxs-lookup"><span data-stu-id="f457a-119">IUnknown Methods</span></span>                                        | <span data-ttu-id="f457a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f457a-120">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="f457a-121">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="f457a-121">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="f457a-122">Restituisce puntatori alle interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="f457a-122">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="f457a-123">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="f457a-123">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="f457a-124">Incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="f457a-124">Increments reference count.</span></span>               |
| [<span data-ttu-id="f457a-125">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="f457a-125">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="f457a-126">Riduce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="f457a-126">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="f457a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f457a-127">Requirements</span></span>



| <span data-ttu-id="f457a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f457a-128">Requirement</span></span> | <span data-ttu-id="f457a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f457a-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f457a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f457a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f457a-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f457a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f457a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f457a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f457a-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f457a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f457a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f457a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f457a-135"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="f457a-135"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
