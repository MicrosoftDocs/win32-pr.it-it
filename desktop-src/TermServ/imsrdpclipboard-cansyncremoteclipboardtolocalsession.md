---
title: Metodo IMsRdpClipboard CanSyncRemoteClipboardToLocalSession
description: Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CanSyncRemoteClipboardToLocalSession
- Metodo CanSyncRemoteClipboardToLocalSession Servizi Desktop remoto, interfaccia IMsRdpClipboard
- Interfaccia IMsRdpClipboard Servizi Desktop remoto, metodo CanSyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303661"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="a6359-106">Metodo IMsRdpClipboard:: CanSyncRemoteClipboardToLocalSession</span><span class="sxs-lookup"><span data-stu-id="a6359-106">IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="a6359-107">Indica se gli Appunti remoti possono essere sincronizzati con la sessione locale.</span><span class="sxs-lookup"><span data-stu-id="a6359-107">Indicates whether the remote Clipboard can be synced to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6359-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6359-108">Syntax</span></span>

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="a6359-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6359-109">Parameters</span></span>

<span data-ttu-id="a6359-110">**True** se gli Appunti remoti possono essere sincronizzati con la sessione locale; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a6359-110">**TRUE** if the remote Clipboard can be synced to the local session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6359-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6359-111">Return value</span></span>

<span data-ttu-id="a6359-112">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="a6359-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6359-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6359-113">Requirements</span></span>

| <span data-ttu-id="a6359-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6359-114">Requirement</span></span> | <span data-ttu-id="a6359-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a6359-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="a6359-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6359-116">Minimum supported client</span></span>| <span data-ttu-id="a6359-117">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="a6359-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="a6359-118">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a6359-118">Type library</span></span>            | <span data-ttu-id="a6359-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="a6359-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="a6359-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a6359-120">DLL</span></span>                  | <span data-ttu-id="a6359-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="a6359-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="a6359-122">IID</span><span class="sxs-lookup"><span data-stu-id="a6359-122">IID</span></span>                      | <span data-ttu-id="a6359-123">IID \_ IMsRdpClipboard è definito come 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="a6359-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="a6359-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6359-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6359-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="a6359-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>