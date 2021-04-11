---
title: Interfaccia IMsRdpClipboard
description: Rappresenta il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClipboard Servizi Desktop remoto
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123300"
---
# <a name="imsrdpclipboard-interface"></a><span data-ttu-id="c81e4-105">Interfaccia IMsRdpClipboard</span><span class="sxs-lookup"><span data-stu-id="c81e4-105">IMsRdpClipboard interface</span></span>

<span data-ttu-id="c81e4-106">Rappresenta il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti, ovvero se il valore della proprietà [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="c81e4-106">Represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="members"></a><span data-ttu-id="c81e4-107">Membri</span><span class="sxs-lookup"><span data-stu-id="c81e4-107">Members</span></span>

<span data-ttu-id="c81e4-108">L'interfaccia **IMsRdpClipboard** eredita da **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="c81e4-108">The **IMsRdpClipboard** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="c81e4-109">**IMsRdpClipboard** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c81e4-109">**IMsRdpClipboard** also has these types of members:</span></span>

- [<span data-ttu-id="c81e4-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="c81e4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c81e4-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c81e4-111">Methods</span></span>

<span data-ttu-id="c81e4-112">L'interfaccia **IMsRdpClipboard** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c81e4-112">The **IMsRdpClipboard** interface has these methods.</span></span>


| <span data-ttu-id="c81e4-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="c81e4-113">Method</span></span>        | <span data-ttu-id="c81e4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c81e4-114">Description</span></span>      |
|:---------------|:----------------|
| [<span data-ttu-id="c81e4-115">**CanSyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="c81e4-115">**CanSyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  <span data-ttu-id="c81e4-116">Indica se gli Appunti locali possono essere sincronizzati con la sessione remota.</span><span class="sxs-lookup"><span data-stu-id="c81e4-116">Indicates whether the local Clipboard can be synced to the remote session.</span></span>                   |
| [<span data-ttu-id="c81e4-117">**CanSyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="c81e4-117">**CanSyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  <span data-ttu-id="c81e4-118">Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.</span><span class="sxs-lookup"><span data-stu-id="c81e4-118">Indicates whether the remote Clipboard can be synced to the local session.</span></span>                   |
| [<span data-ttu-id="c81e4-119">**SyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="c81e4-119">**SyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  <span data-ttu-id="c81e4-120">Sincronizza gli Appunti locali con la sessione remota.</span><span class="sxs-lookup"><span data-stu-id="c81e4-120">Syncs the local Clipboard to the remote session.</span></span>                   |
| [<span data-ttu-id="c81e4-121">**SyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="c81e4-121">**SyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   <span data-ttu-id="c81e4-122">Sincronizza gli Appunti remoti nella sessione locale.</span><span class="sxs-lookup"><span data-stu-id="c81e4-122">Syncs the remote Clipboard to the local session.</span></span>                      |

## <a name="requirements"></a><span data-ttu-id="c81e4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c81e4-123">Requirements</span></span>

| <span data-ttu-id="c81e4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c81e4-124">Requirement</span></span> | <span data-ttu-id="c81e4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c81e4-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="c81e4-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c81e4-126">Minimum supported client</span></span>| <span data-ttu-id="c81e4-127">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="c81e4-127">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="c81e4-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c81e4-128">Type library</span></span>            | <span data-ttu-id="c81e4-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c81e4-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="c81e4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c81e4-130">DLL</span></span>                  | <span data-ttu-id="c81e4-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c81e4-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="c81e4-132">IID</span><span class="sxs-lookup"><span data-stu-id="c81e4-132">IID</span></span>                      | <span data-ttu-id="c81e4-133">IID \_ IMsRdpClipboard è definito come 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="c81e4-133">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>            |

## <a name="see-also"></a><span data-ttu-id="c81e4-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c81e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81e4-135">**IMsRdpClientNonScriptable7:: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="c81e4-135">**IMsRdpClientNonScriptable7::Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
