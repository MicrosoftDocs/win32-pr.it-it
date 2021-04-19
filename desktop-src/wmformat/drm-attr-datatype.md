---
title: Enumerazione DRM_ATTR_DATATYPE (wmdrmsdk. h)
description: L' \_ \_ enumerazione di tipo di dati DRM attr definisce i tipi di dati utilizzati per le proprietà e gli attributi DRM.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- Formato Windows Media enumerazione DRM_ATTR_DATATYPE
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e684ba1c09a86c65a13adbd189bb185f65598b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332289"
---
# <a name="drm_attr_datatype-enumeration"></a><span data-ttu-id="547f2-105">\_ \_ Enumerazione DataType attr DRM</span><span class="sxs-lookup"><span data-stu-id="547f2-105">DRM\_ATTR\_DATATYPE enumeration</span></span>

<span data-ttu-id="547f2-106">L'enumerazione di **\_ \_ tipo di dati DRM attr** definisce i tipi di dati utilizzati per le proprietà e gli attributi DRM.</span><span class="sxs-lookup"><span data-stu-id="547f2-106">The **DRM\_ATTR\_DATATYPE** enumeration defines the data types used for DRM attributes and properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="547f2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="547f2-107">Syntax</span></span>


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="547f2-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="547f2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="547f2-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**tipo di DRM \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="547f2-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="547f2-110">La proprietà è un valore **DWORD** a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="547f2-110">The property is a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="547f2-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_stringa di tipo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="547f2-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="547f2-112">La proprietà è una stringa Unicode con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="547f2-112">The property is a null-terminated Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="547f2-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**\_Binary di tipo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="547f2-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="547f2-114">La proprietà è una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="547f2-114">The property is an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="547f2-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**\_tipo DRM \_ bool**</span><span class="sxs-lookup"><span data-stu-id="547f2-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="547f2-116">La proprietà è un valore booleano a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="547f2-116">The property is a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="547f2-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**\_QWORD di tipo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="547f2-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="547f2-118">La proprietà è un valore **QWORD** a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="547f2-118">The property is an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="547f2-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**\_parola di tipo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="547f2-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="547f2-120">La proprietà è un valore **Word** a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="547f2-120">The property is a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="547f2-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID di tipo DRM \_**</span><span class="sxs-lookup"><span data-stu-id="547f2-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="547f2-122">La proprietà è un valore GUID a 128 bit (6 byte).</span><span class="sxs-lookup"><span data-stu-id="547f2-122">The property is a 128-bit (6-byte) GUID value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="547f2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="547f2-123">Requirements</span></span>



| <span data-ttu-id="547f2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="547f2-124">Requirement</span></span> | <span data-ttu-id="547f2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="547f2-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="547f2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="547f2-126">Header</span></span><br/> | <dl> <span data-ttu-id="547f2-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="547f2-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="547f2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="547f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="547f2-129">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="547f2-129">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





