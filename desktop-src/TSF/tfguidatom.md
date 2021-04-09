---
title: TfGuidAtom (msctf. h)
description: Il tipo di dati TfGuidAtom identifica un GUID in TSF. Un TfGuidAtom viene ottenuto chiamando ITfCategoryMgr RegisterGUID.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- TfGuidAtom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118934"
---
# <a name="tfguidatom"></a><span data-ttu-id="8a1d0-105">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="8a1d0-105">TfGuidAtom</span></span>

<span data-ttu-id="8a1d0-106">Il tipo di dati **TfGuidAtom** identifica un **GUID** in TSF.</span><span class="sxs-lookup"><span data-stu-id="8a1d0-106">The **TfGuidAtom** data type identifies a **GUID** within TSF.</span></span> <span data-ttu-id="8a1d0-107">Un **TfGuidAtom** viene ottenuto chiamando [**ITfCategoryMgr:: RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="8a1d0-107">A **TfGuidAtom** is obtained by calling [**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a><span data-ttu-id="8a1d0-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a1d0-108">Remarks</span></span>

<span data-ttu-id="8a1d0-109">Un valore **TfGuidAtom** è valido solo all'interno del processo da cui viene chiamato **ITfCategoryMgr:: RegisterGUID** .</span><span class="sxs-lookup"><span data-stu-id="8a1d0-109">A **TfGuidAtom** value is only valid within the process that **ITfCategoryMgr::RegisterGUID** is called from.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a1d0-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a1d0-110">Requirements</span></span>



| <span data-ttu-id="8a1d0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a1d0-111">Requirement</span></span> | <span data-ttu-id="8a1d0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8a1d0-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1d0-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a1d0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8a1d0-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8a1d0-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8a1d0-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a1d0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8a1d0-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8a1d0-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8a1d0-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="8a1d0-117">Redistributable</span></span><br/>          | <span data-ttu-id="8a1d0-118">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8a1d0-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="8a1d0-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a1d0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a1d0-120"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a1d0-120"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a1d0-121">IDL</span><span class="sxs-lookup"><span data-stu-id="8a1d0-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a1d0-122"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a1d0-122"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a1d0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a1d0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1d0-124">**ITfCategoryMgr:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="8a1d0-124">**ITfCategoryMgr::GetGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="8a1d0-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span><span class="sxs-lookup"><span data-stu-id="8a1d0-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[<span data-ttu-id="8a1d0-126">**ITfCategoryMgr::RegisterGUID**</span><span class="sxs-lookup"><span data-stu-id="8a1d0-126">**ITfCategoryMgr::RegisterGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





