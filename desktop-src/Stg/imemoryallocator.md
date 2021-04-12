---
title: Classe IMemoryAllocator
description: Implementato dall'allocatore di memoria per la funzione StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Archiviazione strutturata della classe IMemoryAllocator
- Archiviazione strutturata della classe IMemoryAllocator, descritta
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400677"
---
# <a name="imemoryallocator-class"></a><span data-ttu-id="0d69c-105">Classe IMemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="0d69c-105">IMemoryAllocator class</span></span>

<span data-ttu-id="0d69c-106">La classe **IMemoryAllocator** viene implementata dall'allocatore di memoria per la funzione [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="0d69c-106">The **IMemoryAllocator** class is implemented by the memory allocator for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="methods"></a><span data-ttu-id="0d69c-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="0d69c-107">Methods</span></span>



| <span data-ttu-id="0d69c-108">Nome</span><span class="sxs-lookup"><span data-stu-id="0d69c-108">Name</span></span>                                                     | <span data-ttu-id="0d69c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d69c-109">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d69c-110">**Allocare**</span><span class="sxs-lookup"><span data-stu-id="0d69c-110">**Allocate**</span></span>](imemoryallocator-allocate.md)<br/> | <span data-ttu-id="0d69c-111">Alloca memoria per la funzione [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) quando la funzione converte un tipo di dati **SERIALIZEDPROPERTYVALUE** in un tipo di dati **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="0d69c-111">Allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span><br/> |
| [<span data-ttu-id="0d69c-112">**Gratuito**</span><span class="sxs-lookup"><span data-stu-id="0d69c-112">**Free**</span></span>](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | <span data-ttu-id="0d69c-113">Libera la memoria allocata dal metodo [**allocate**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="0d69c-113">Frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span><br/>                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="0d69c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d69c-114">Remarks</span></span>

<span data-ttu-id="0d69c-115">Questa classe viene utilizzata solo dalla funzione [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="0d69c-115">This class is only used by the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d69c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d69c-116">Requirements</span></span>



| <span data-ttu-id="0d69c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d69c-117">Requirement</span></span> | <span data-ttu-id="0d69c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0d69c-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d69c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d69c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0d69c-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d69c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0d69c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d69c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0d69c-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d69c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0d69c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d69c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d69c-124"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d69c-124"><dt>Ole32.lib</dt></span></span> </dl> |



 

