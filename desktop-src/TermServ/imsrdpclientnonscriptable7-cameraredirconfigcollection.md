---
title: Proprietà CameraRedirConfigCollection di IMsRdpClientNonScriptable7
description: Ottiene la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CameraRedirConfigCollection
- Servizi Desktop remoto proprietà CameraRedirConfigCollection, interfaccia IMsRdpClientNonScriptable7
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto, proprietà CameraRedirConfigCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104341396"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a><span data-ttu-id="86123-106">Proprietà IMsRdpClientNonScriptable7:: CameraRedirConfigCollection</span><span class="sxs-lookup"><span data-stu-id="86123-106">IMsRdpClientNonScriptable7::CameraRedirConfigCollection property</span></span>

<span data-ttu-id="86123-107">Ottiene la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="86123-107">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

<span data-ttu-id="86123-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="86123-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="86123-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86123-109">Syntax</span></span>


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a><span data-ttu-id="86123-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="86123-110">Property value</span></span>

<span data-ttu-id="86123-111">Oggetto [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) che rappresenta la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="86123-111">An [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) that represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="86123-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86123-112">Requirements</span></span>

| <span data-ttu-id="86123-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="86123-113">Requirement</span></span> | <span data-ttu-id="86123-114">Valore</span><span class="sxs-lookup"><span data-stu-id="86123-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="86123-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86123-115">Minimum supported client</span></span>| <span data-ttu-id="86123-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="86123-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="86123-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="86123-117">Type library</span></span>            | <span data-ttu-id="86123-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="86123-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="86123-119">DLL</span><span class="sxs-lookup"><span data-stu-id="86123-119">DLL</span></span>                  | <span data-ttu-id="86123-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="86123-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="86123-121">IID</span><span class="sxs-lookup"><span data-stu-id="86123-121">IID</span></span>                      | <span data-ttu-id="86123-122">IID \_ IMsRdpClientNonScriptable7 è definito come 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="86123-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="86123-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86123-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86123-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="86123-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>