---
title: Metodo IMsRdpClipboard SyncRemoteClipboardToLocalSession
description: Sincronizza gli Appunti remoti nella sessione locale.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SyncRemoteClipboardToLocalSession
- Metodo SyncRemoteClipboardToLocalSession Servizi Desktop remoto, interfaccia IMsRdpClipboard
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, metodo SyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d397d7c1ca4407a5125877721be9aa022f8132a7
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520322"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="8ef6d-106">Metodo IMsRdpClipboard:: SyncRemoteClipboardToLocalSession</span><span class="sxs-lookup"><span data-stu-id="8ef6d-106">IMsRdpClipboard::SyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="8ef6d-107">Sincronizza gli Appunti remoti nella sessione locale.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-107">Syncs the remote Clipboard to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef6d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ef6d-108">Syntax</span></span>

```C++
HRESULT SyncRemoteClipboardToLocalSession();
```

## <a name="parameters"></a><span data-ttu-id="8ef6d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ef6d-109">Parameters</span></span>

<span data-ttu-id="8ef6d-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8ef6d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ef6d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ef6d-111">Return value</span></span>

<span data-ttu-id="8ef6d-112">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="8ef6d-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef6d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ef6d-113">Requirements</span></span>

| <span data-ttu-id="8ef6d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ef6d-114">Requirement</span></span> | <span data-ttu-id="8ef6d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8ef6d-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="8ef6d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ef6d-116">Minimum supported client</span></span>| <span data-ttu-id="8ef6d-117">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="8ef6d-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="8ef6d-118">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8ef6d-118">Type library</span></span>            | <span data-ttu-id="8ef6d-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="8ef6d-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="8ef6d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8ef6d-120">DLL</span></span>                  | <span data-ttu-id="8ef6d-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="8ef6d-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="8ef6d-122">IID</span><span class="sxs-lookup"><span data-stu-id="8ef6d-122">IID</span></span>                      | <span data-ttu-id="8ef6d-123">IID \_ IMsRdpClipboard è definito come 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="8ef6d-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="8ef6d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ef6d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef6d-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="8ef6d-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>