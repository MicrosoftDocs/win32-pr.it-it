---
description: Contiene informazioni di base sul modulo.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: Struttura AUX_MODULE_BASIC_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330559"
---
# <a name="aux_module_basic_info-structure"></a><span data-ttu-id="44066-103">\_Struttura delle \_ informazioni di base del modulo aux \_</span><span class="sxs-lookup"><span data-stu-id="44066-103">AUX\_MODULE\_BASIC\_INFO structure</span></span>

<span data-ttu-id="44066-104">Contiene informazioni di base sul modulo.</span><span class="sxs-lookup"><span data-stu-id="44066-104">Contains basic module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="44066-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44066-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a><span data-ttu-id="44066-106">Members</span><span class="sxs-lookup"><span data-stu-id="44066-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="44066-107">**ImageBase sul**</span><span class="sxs-lookup"><span data-stu-id="44066-107">**ImageBase**</span></span>
</dt> <dd>

<span data-ttu-id="44066-108">Indirizzo di base del modulo nello spazio degli indirizzi del kernel.</span><span class="sxs-lookup"><span data-stu-id="44066-108">The base address of the module within the kernel's address space.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44066-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="44066-109">Remarks</span></span>

<span data-ttu-id="44066-110">La libreria di oggetti che implementa questa API può essere scaricata da [qui](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="44066-110">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="44066-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44066-111">Requirements</span></span>



| <span data-ttu-id="44066-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="44066-112">Requirement</span></span> | <span data-ttu-id="44066-113">Valore</span><span class="sxs-lookup"><span data-stu-id="44066-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44066-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="44066-114">Redistributable</span></span><br/> | <span data-ttu-id="44066-115">Libreria API ausiliaria Windows versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="44066-115">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="44066-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44066-116">Header</span></span><br/>          | <dl> <span data-ttu-id="44066-117"><dt>Aux \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="44066-117"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44066-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44066-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44066-119">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="44066-119">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




