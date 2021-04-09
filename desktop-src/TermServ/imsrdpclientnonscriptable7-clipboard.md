---
title: Proprietà degli Appunti IMsRdpClientNonScriptable7
description: Ottiene il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà degli Appunti
- Servizi Desktop remoto proprietà degli Appunti, interfaccia IMsRdpClientNonScriptable7
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto, proprietà degli Appunti
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "103965441"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a><span data-ttu-id="f36bd-106">Proprietà IMsRdpClientNonScriptable7:: Clipboard</span><span class="sxs-lookup"><span data-stu-id="f36bd-106">IMsRdpClientNonScriptable7::Clipboard property</span></span>

<span data-ttu-id="f36bd-107">Ottiene il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="f36bd-107">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>

<span data-ttu-id="f36bd-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f36bd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36bd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f36bd-109">Syntax</span></span>

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a><span data-ttu-id="f36bd-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f36bd-110">Property value</span></span>

<span data-ttu-id="f36bd-111">Un [IMsRdpClipboard](imsrdpclipboard.md) che rappresenta il controller degli Appunti usato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti, ovvero se il valore della proprietà [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="f36bd-111">An [IMsRdpClipboard](imsrdpclipboard.md) that represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="requirements"></a><span data-ttu-id="f36bd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f36bd-112">Requirements</span></span>

| <span data-ttu-id="f36bd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36bd-113">Requirement</span></span> | <span data-ttu-id="f36bd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f36bd-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f36bd-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f36bd-115">Minimum supported client</span></span>| <span data-ttu-id="f36bd-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="f36bd-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f36bd-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f36bd-117">Type library</span></span>            | <span data-ttu-id="f36bd-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f36bd-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f36bd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f36bd-119">DLL</span></span>                  | <span data-ttu-id="f36bd-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f36bd-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f36bd-121">IID</span><span class="sxs-lookup"><span data-stu-id="f36bd-121">IID</span></span>                      | <span data-ttu-id="f36bd-122">IID \_ IMsRdpClientNonScriptable7 è definito come 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="f36bd-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="f36bd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f36bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36bd-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="f36bd-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>