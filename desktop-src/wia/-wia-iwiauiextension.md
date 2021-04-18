---
description: L'interfaccia IWiaUIExtension fornisce metodi che sostituiscono l'interfaccia utente di sistema predefinita, forniscono un logo bitmap personalizzato del dispositivo e forniscono un'icona personalizzata del dispositivo.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Interfaccia IWiaUIExtension (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307346"
---
# <a name="iwiauiextension-interface"></a><span data-ttu-id="192f1-103">Interfaccia IWiaUIExtension</span><span class="sxs-lookup"><span data-stu-id="192f1-103">IWiaUIExtension interface</span></span>

<span data-ttu-id="192f1-104">L'interfaccia **IWiaUIExtension** fornisce metodi che sostituiscono l'interfaccia utente di sistema predefinita, forniscono un logo bitmap personalizzato del dispositivo e forniscono un'icona personalizzata del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="192f1-104">The **IWiaUIExtension** interface provides methods that replace the default system user interface, provide a custom device bitmap logo, and provide a custom device icon.</span></span>

## <a name="members"></a><span data-ttu-id="192f1-105">Membri</span><span class="sxs-lookup"><span data-stu-id="192f1-105">Members</span></span>

<span data-ttu-id="192f1-106">L'interfaccia **IWiaUIExtension** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="192f1-106">The **IWiaUIExtension** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="192f1-107">**IWiaUIExtension** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="192f1-107">**IWiaUIExtension** also has these types of members:</span></span>

-   [<span data-ttu-id="192f1-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="192f1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="192f1-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="192f1-109">Methods</span></span>

<span data-ttu-id="192f1-110">L'interfaccia **IWiaUIExtension** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="192f1-110">The **IWiaUIExtension** interface has these methods.</span></span>



| <span data-ttu-id="192f1-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="192f1-111">Method</span></span>                                                                  | <span data-ttu-id="192f1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="192f1-112">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="192f1-113">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="192f1-113">**DeviceDialog**</span></span>](-wia-iwiauiextension-devicedialog.md)               | <span data-ttu-id="192f1-114">Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="192f1-114">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="192f1-115">**GetDeviceBitmapLogo**</span><span class="sxs-lookup"><span data-stu-id="192f1-115">**GetDeviceBitmapLogo**</span></span>](-wia-iwiauiextension-getdevicebitmaplogo.md) | <span data-ttu-id="192f1-116">Ottiene un logo bitmap personalizzato per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="192f1-116">Gets a custom bitmap logo for the device.</span></span><br/>                                         |
| [<span data-ttu-id="192f1-117">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="192f1-117">**GetDeviceIcon**</span></span>](-wia-iwiauiextension-getdeviceicon.md)             | <span data-ttu-id="192f1-118">Ottiene un'icona di dispositivo personalizzata.</span><span class="sxs-lookup"><span data-stu-id="192f1-118">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="192f1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="192f1-119">Remarks</span></span>



| <span data-ttu-id="192f1-120">Metodi IUnknown</span><span class="sxs-lookup"><span data-stu-id="192f1-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="192f1-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="192f1-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="192f1-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="192f1-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="192f1-123">Restituisce puntatori alle interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="192f1-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="192f1-124">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="192f1-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="192f1-125">Incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="192f1-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="192f1-126">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="192f1-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="192f1-127">Riduce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="192f1-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="192f1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="192f1-128">Requirements</span></span>



| <span data-ttu-id="192f1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="192f1-129">Requirement</span></span> | <span data-ttu-id="192f1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="192f1-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="192f1-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="192f1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="192f1-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="192f1-132">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="192f1-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="192f1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="192f1-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="192f1-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="192f1-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="192f1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="192f1-136"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="192f1-136"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
