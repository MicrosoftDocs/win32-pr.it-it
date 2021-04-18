---
title: Metodo allocate IMemoryAllocator
description: Il metodo allocate alloca memoria per la funzione StgConvertPropertyToVariant quando la funzione converte un tipo di dati SERIALIZEDPROPERTYVALUE in un tipo di dati PROPVARIANT.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Allocare l'archiviazione strutturata del metodo
- Allocare l'archiviazione strutturata del metodo, interfaccia IMemoryAllocator
- Archiviazione strutturata dell'interfaccia IMemoryAllocator, metodo allocate
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300950"
---
# <a name="imemoryallocatorallocate-method"></a><span data-ttu-id="8da51-106">Metodo IMemoryAllocator:: allocate</span><span class="sxs-lookup"><span data-stu-id="8da51-106">IMemoryAllocator::Allocate method</span></span>

<span data-ttu-id="8da51-107">Il metodo **allocate** alloca memoria per la funzione [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando la funzione converte un tipo di dati **SERIALIZEDPROPERTYVALUE** in un tipo di dati **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="8da51-107">The **Allocate** method allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da51-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8da51-108">Syntax</span></span>


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="8da51-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8da51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da51-110">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8da51-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da51-111">Specifica le dimensioni della memoria da allocare.</span><span class="sxs-lookup"><span data-stu-id="8da51-111">Specifies the size of memory to be allocated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8da51-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8da51-112">Requirements</span></span>



| <span data-ttu-id="8da51-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da51-113">Requirement</span></span> | <span data-ttu-id="8da51-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8da51-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8da51-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8da51-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8da51-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8da51-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8da51-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8da51-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8da51-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8da51-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8da51-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="8da51-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="8da51-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8da51-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

