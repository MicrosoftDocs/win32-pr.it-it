---
description: Fornisce la funzionalità per ottenere IMFDXGIDeviceManager dall'Microsoft Media Foundation sink di rendering video.
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: Interfaccia IMFDXGIDeviceManagerSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753191"
---
# <a name="imfdxgidevicemanagersource-interface"></a><span data-ttu-id="27196-103">Interfaccia IMFDXGIDeviceManagerSource</span><span class="sxs-lookup"><span data-stu-id="27196-103">IMFDXGIDeviceManagerSource interface</span></span>

<span data-ttu-id="27196-104">Fornisce la funzionalità per ottenere [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) dall'Microsoft Media Foundation sink di rendering video.</span><span class="sxs-lookup"><span data-stu-id="27196-104">Provides functionality for getting the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="members"></a><span data-ttu-id="27196-105">Membri</span><span class="sxs-lookup"><span data-stu-id="27196-105">Members</span></span>

<span data-ttu-id="27196-106">L'interfaccia **IMFDXGIDeviceManagerSource** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="27196-106">The **IMFDXGIDeviceManagerSource** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="27196-107">**IMFDXGIDeviceManagerSource** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="27196-107">**IMFDXGIDeviceManagerSource** also has these types of members:</span></span>

-   [<span data-ttu-id="27196-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="27196-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="27196-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="27196-109">Methods</span></span>

<span data-ttu-id="27196-110">L'interfaccia **IMFDXGIDeviceManagerSource** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="27196-110">The **IMFDXGIDeviceManagerSource** interface has these methods.</span></span>



| <span data-ttu-id="27196-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="27196-111">Method</span></span>                                                      | <span data-ttu-id="27196-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27196-112">Description</span></span>                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27196-113">**GetManager**</span><span class="sxs-lookup"><span data-stu-id="27196-113">**GetManager**</span></span>](imfdxgidevicemanagersource-getmanager.md) | <span data-ttu-id="27196-114">Ottiene [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) dal sink di rendering del video Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="27196-114">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Media Foundation video rendering sink.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="27196-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27196-115">Requirements</span></span>



| <span data-ttu-id="27196-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="27196-116">Requirement</span></span> | <span data-ttu-id="27196-117">Valore</span><span class="sxs-lookup"><span data-stu-id="27196-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27196-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27196-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27196-119">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="27196-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="27196-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27196-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27196-121">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="27196-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="27196-122">IDL</span><span class="sxs-lookup"><span data-stu-id="27196-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27196-123"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27196-123"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27196-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27196-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27196-125">Interfacce di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27196-125">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
