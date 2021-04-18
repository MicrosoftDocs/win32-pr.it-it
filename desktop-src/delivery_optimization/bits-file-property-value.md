---
title: Struttura BITS_FILE_PROPERTY_VALUE (Deliveryoptimization. h)
description: Il BITS_FILE_PROPERTY_VALUE Unione fornisce il valore della proprietà del file DO in base a un valore dell'enumerazione BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Struttura BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301090"
---
# <a name="bits_file_property_value-structure"></a><span data-ttu-id="48cf9-104">Struttura BITS_FILE_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="48cf9-104">BITS_FILE_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="48cf9-105">Il **BITS_FILE_PROPERTY_VALUE** Unione fornisce il valore della proprietà del file do in base a un valore dell'enumerazione [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .</span><span class="sxs-lookup"><span data-stu-id="48cf9-105">The **BITS_FILE_PROPERTY_VALUE** union provides the property value of the DO file based on a value from the [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="48cf9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48cf9-106">Syntax</span></span>


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="48cf9-107">Members</span><span class="sxs-lookup"><span data-stu-id="48cf9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="48cf9-108">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="48cf9-108">**String**</span></span>
</dt> <dd>

<span data-ttu-id="48cf9-109">Questo valore viene usato quando si usa il valore enum di ID proprietà **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span><span class="sxs-lookup"><span data-stu-id="48cf9-109">This value is used when using the property ID enum value **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48cf9-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48cf9-110">Requirements</span></span>



| <span data-ttu-id="48cf9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="48cf9-111">Requirement</span></span> | <span data-ttu-id="48cf9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="48cf9-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48cf9-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48cf9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="48cf9-114">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="48cf9-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="48cf9-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48cf9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="48cf9-116">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="48cf9-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="48cf9-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48cf9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="48cf9-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="48cf9-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48cf9-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48cf9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48cf9-120">**BITS_FILE_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="48cf9-120">**BITS_FILE_PROPERTY_ID**</span></span>](bits-file-property-id-.md)
</dt> <dt>

[<span data-ttu-id="48cf9-121">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="48cf9-121">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[<span data-ttu-id="48cf9-122">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="48cf9-122">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





