---
title: Metodo IMsRdpClipboard CanSyncLocalClipboardToRemoteSession
description: Indica se gli Appunti locali possono essere sincronizzati con la sessione remota.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CanSyncLocalClipboardToRemoteSession
- Metodo CanSyncLocalClipboardToRemoteSession Servizi Desktop remoto, interfaccia IMsRdpClipboard
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, metodo CanSyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303648"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a><span data-ttu-id="fa7dc-106">Metodo IMsRdpClipboard:: CanSyncLocalClipboardToRemoteSession</span><span class="sxs-lookup"><span data-stu-id="fa7dc-106">IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession method</span></span>

<span data-ttu-id="fa7dc-107">Indica se gli Appunti locali possono essere sincronizzati con la sessione remota.</span><span class="sxs-lookup"><span data-stu-id="fa7dc-107">Indicates whether the local Clipboard can be synced to the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa7dc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa7dc-108">Syntax</span></span>

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="fa7dc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa7dc-109">Parameters</span></span>

<span data-ttu-id="fa7dc-110">**True** se gli Appunti locali possono essere sincronizzati con la sessione remota. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="fa7dc-110">**TRUE** if the local Clipboard can be synced to the remote session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa7dc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa7dc-111">Return value</span></span>

<span data-ttu-id="fa7dc-112">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="fa7dc-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa7dc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa7dc-113">Requirements</span></span>

| <span data-ttu-id="fa7dc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa7dc-114">Requirement</span></span> | <span data-ttu-id="fa7dc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fa7dc-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="fa7dc-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa7dc-116">Minimum supported client</span></span>| <span data-ttu-id="fa7dc-117">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="fa7dc-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="fa7dc-118">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fa7dc-118">Type library</span></span>            | <span data-ttu-id="fa7dc-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fa7dc-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="fa7dc-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fa7dc-120">DLL</span></span>                  | <span data-ttu-id="fa7dc-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fa7dc-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="fa7dc-122">IID</span><span class="sxs-lookup"><span data-stu-id="fa7dc-122">IID</span></span>                      | <span data-ttu-id="fa7dc-123">IID \_ IMsRdpClipboard è definito come 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="fa7dc-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="fa7dc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa7dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa7dc-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="fa7dc-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>