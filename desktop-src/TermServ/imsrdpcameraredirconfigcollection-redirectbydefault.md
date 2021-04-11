---
title: Proprietà RedirectByDefault di IMsRdpCameraRedirConfigCollection
description: Specifica se una nuova fotocamera viene reindirizzata per impostazione predefinita.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectByDefault
- Servizi Desktop remoto proprietà RedirectByDefault, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, proprietà RedirectByDefault
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123285"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a><span data-ttu-id="71b56-106">Proprietà IMsRdpCameraRedirConfigCollection:: RedirectByDefault</span><span class="sxs-lookup"><span data-stu-id="71b56-106">IMsRdpCameraRedirConfigCollection::RedirectByDefault property</span></span>

<span data-ttu-id="71b56-107">Specifica se una nuova fotocamera viene reindirizzata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="71b56-107">Specifies whether or not any new camera gets redirected by default.</span></span>

<span data-ttu-id="71b56-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="71b56-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b56-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71b56-109">Syntax</span></span>

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a><span data-ttu-id="71b56-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="71b56-110">Property value</span></span>

<span data-ttu-id="71b56-111">Valore che indica se una nuova fotocamera viene reindirizzata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="71b56-111">A value that indicates whether or not any new camera gets redirected by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b56-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71b56-112">Requirements</span></span>

| <span data-ttu-id="71b56-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="71b56-113">Requirement</span></span> | <span data-ttu-id="71b56-114">Valore</span><span class="sxs-lookup"><span data-stu-id="71b56-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="71b56-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71b56-115">Minimum supported client</span></span>| <span data-ttu-id="71b56-116">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="71b56-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="71b56-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="71b56-117">Type library</span></span>            | <span data-ttu-id="71b56-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="71b56-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="71b56-119">DLL</span><span class="sxs-lookup"><span data-stu-id="71b56-119">DLL</span></span>                  | <span data-ttu-id="71b56-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="71b56-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="71b56-121">IID</span><span class="sxs-lookup"><span data-stu-id="71b56-121">IID</span></span>                      | <span data-ttu-id="71b56-122">IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="71b56-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="71b56-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71b56-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b56-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="71b56-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>