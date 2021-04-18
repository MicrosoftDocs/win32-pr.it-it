---
title: Proprietà Enabled di IRemoteDesktopClientTouchPointer
description: Indica se la funzionalità del puntatore a tocco è abilitata nel controllo client del contenitore di app RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà abilitata
- Servizi Desktop remoto proprietà Enabled, interfaccia IRemoteDesktopClientTouchPointer
- Interfaccia IRemoteDesktopClientTouchPointer Servizi Desktop remoto, proprietà Enabled
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301982"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a><span data-ttu-id="213bd-106">Proprietà IRemoteDesktopClientTouchPointer:: Enabled</span><span class="sxs-lookup"><span data-stu-id="213bd-106">IRemoteDesktopClientTouchPointer::Enabled property</span></span>

<span data-ttu-id="213bd-107">Indica se la funzionalità del puntatore a tocco è abilitata nel controllo client del contenitore di app RDP.</span><span class="sxs-lookup"><span data-stu-id="213bd-107">Whether the touch pointer feature is enabled on the RDP app container client control.</span></span>

<span data-ttu-id="213bd-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="213bd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="213bd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="213bd-109">Syntax</span></span>


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="213bd-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="213bd-110">Property value</span></span>

<span data-ttu-id="213bd-111">**true** se la funzionalità del puntatore a tocco è abilitata; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="213bd-111">**true** if the touch pointer feature is enabled; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="213bd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="213bd-112">Requirements</span></span>



| <span data-ttu-id="213bd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="213bd-113">Requirement</span></span> | <span data-ttu-id="213bd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="213bd-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="213bd-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="213bd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="213bd-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="213bd-116">Windows 8</span></span><br/>                                                                                |
| <span data-ttu-id="213bd-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="213bd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="213bd-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="213bd-118">Windows Server 2012</span></span><br/>                                                                      |
| <span data-ttu-id="213bd-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="213bd-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="213bd-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="213bd-120"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="213bd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="213bd-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="213bd-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="213bd-122"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="213bd-123">IID</span><span class="sxs-lookup"><span data-stu-id="213bd-123">IID</span></span><br/>                      | <span data-ttu-id="213bd-124">IID \_ IRemoteDesktopClientTouchPointer è definito come 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span><span class="sxs-lookup"><span data-stu-id="213bd-124">IID\_IRemoteDesktopClientTouchPointer is defined as 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="213bd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="213bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="213bd-126">**IRemoteDesktopClientTouchPointer**</span><span class="sxs-lookup"><span data-stu-id="213bd-126">**IRemoteDesktopClientTouchPointer**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

