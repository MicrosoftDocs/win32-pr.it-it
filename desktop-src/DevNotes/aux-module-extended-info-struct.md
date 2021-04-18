---
description: Contiene informazioni estese sul modulo.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: Struttura AUX_MODULE_EXTENDED_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331719"
---
# <a name="aux_module_extended_info-structure"></a><span data-ttu-id="96ddc-103">\_Struttura di \_ informazioni estese del modulo aux \_</span><span class="sxs-lookup"><span data-stu-id="96ddc-103">AUX\_MODULE\_EXTENDED\_INFO structure</span></span>

<span data-ttu-id="96ddc-104">Contiene informazioni estese sul modulo.</span><span class="sxs-lookup"><span data-stu-id="96ddc-104">Contains extended module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ddc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96ddc-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a><span data-ttu-id="96ddc-106">Members</span><span class="sxs-lookup"><span data-stu-id="96ddc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="96ddc-107">**BasicInfo**</span><span class="sxs-lookup"><span data-stu-id="96ddc-107">**BasicInfo**</span></span>
</dt> <dd>

<span data-ttu-id="96ddc-108">Struttura [**di \_ \_ \_ informazioni di base del modulo aux**](aux-module-basic-info-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="96ddc-108">An [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="96ddc-109">**ImageSize**</span><span class="sxs-lookup"><span data-stu-id="96ddc-109">**ImageSize**</span></span>
</dt> <dd>

<span data-ttu-id="96ddc-110">Dimensione, in byte, del modulo caricato.</span><span class="sxs-lookup"><span data-stu-id="96ddc-110">The size, in bytes, of the loaded module.</span></span>

</dd> <dt>

<span data-ttu-id="96ddc-111">**FileNameOffset**</span><span class="sxs-lookup"><span data-stu-id="96ddc-111">**FileNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="96ddc-112">Offset del nome file all'interno del buffer **FullPathName** .</span><span class="sxs-lookup"><span data-stu-id="96ddc-112">The offset of the file name within the **FullPathName** buffer.</span></span>

</dd> <dt>

<span data-ttu-id="96ddc-113">**FullPathName**</span><span class="sxs-lookup"><span data-stu-id="96ddc-113">**FullPathName**</span></span>
</dt> <dd>

<span data-ttu-id="96ddc-114">Percorso completo del modulo.</span><span class="sxs-lookup"><span data-stu-id="96ddc-114">The full path of the module.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96ddc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="96ddc-115">Remarks</span></span>

<span data-ttu-id="96ddc-116">La libreria di oggetti che implementa questa API può essere scaricata da [qui](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="96ddc-116">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="96ddc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96ddc-117">Requirements</span></span>



| <span data-ttu-id="96ddc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="96ddc-118">Requirement</span></span> | <span data-ttu-id="96ddc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="96ddc-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96ddc-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="96ddc-120">Redistributable</span></span><br/> | <span data-ttu-id="96ddc-121">Libreria API ausiliaria Windows versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="96ddc-121">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="96ddc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96ddc-122">Header</span></span><br/>          | <dl> <span data-ttu-id="96ddc-123"><dt>Aux \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="96ddc-123"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ddc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96ddc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ddc-125">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="96ddc-125">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[<span data-ttu-id="96ddc-126">**\_informazioni di \_ base sul modulo aux \_**</span><span class="sxs-lookup"><span data-stu-id="96ddc-126">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




