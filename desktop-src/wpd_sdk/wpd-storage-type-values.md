---
description: Il \_ tipo di enumerazione dei valori del tipo di archiviazione WPD \_ \_ descrive i diversi tipi di archiviazione di dispositivi portatili Windows.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Enumerazione WPD_STORAGE_TYPE_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328961"
---
# <a name="wpd_storage_type_values-enumeration"></a><span data-ttu-id="5aed9-103">\_ \_ Enumerazione dei valori del tipo di archiviazione WPD \_</span><span class="sxs-lookup"><span data-stu-id="5aed9-103">WPD\_STORAGE\_TYPE\_VALUES enumeration</span></span>

<span data-ttu-id="5aed9-104">Il tipo di enumerazione dei **\_ valori del \_ tipo \_ di archiviazione WPD** descrive i diversi tipi di archiviazione di dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="5aed9-104">The **WPD\_STORAGE\_TYPE\_VALUES** enumeration type describes the different Windows Portable Device storage types.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aed9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5aed9-105">Syntax</span></span>


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a><span data-ttu-id="5aed9-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="5aed9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5aed9-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**tipo di archiviazione WPD non \_ \_ \_ definito**</span><span class="sxs-lookup"><span data-stu-id="5aed9-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD\_STORAGE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="5aed9-108">Lo spazio di archiviazione è di tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="5aed9-108">The storage is of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5aed9-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**\_ \_ \_ ROM fisso tipo di archiviazione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5aed9-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD\_STORAGE\_TYPE\_FIXED\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="5aed9-110">L'archiviazione non è rimovibile e di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5aed9-110">The storage is non-removable and read-only.</span></span>

</dd> <dt>

<span data-ttu-id="5aed9-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_ \_ \_ ROM rimovibile tipo di archiviazione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5aed9-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="5aed9-112">Lo spazio di archiviazione è rimovibile ed è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5aed9-112">The storage is removable and is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="5aed9-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ \_ RAM fissa tipo di archiviazione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5aed9-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD\_STORAGE\_TYPE\_FIXED\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="5aed9-114">L'archiviazione non è rimovibile ed è in grado di essere in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5aed9-114">The storage is non-removable and is read/write capable.</span></span>

</dd> <dt>

<span data-ttu-id="5aed9-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_ \_ \_ RAM rimovibile tipo di archiviazione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5aed9-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="5aed9-116">Lo spazio di archiviazione è rimovibile ed è in grado di essere in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5aed9-116">The storage is removable and is read/write capable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5aed9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5aed9-117">Remarks</span></span>

<span data-ttu-id="5aed9-118">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="5aed9-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aed9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5aed9-119">Requirements</span></span>



| <span data-ttu-id="5aed9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aed9-120">Requirement</span></span> | <span data-ttu-id="5aed9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5aed9-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aed9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5aed9-122">Header</span></span><br/> | <dl> <span data-ttu-id="5aed9-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aed9-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aed9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5aed9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aed9-125">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="5aed9-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




