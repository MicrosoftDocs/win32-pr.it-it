---
description: Recupera le informazioni sul set di moduli attualmente caricato per il sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Funzione AuxKlibQueryModuleInformation (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325406"
---
# <a name="auxklibquerymoduleinformation-function"></a><span data-ttu-id="de72b-103">AuxKlibQueryModuleInformation (funzione)</span><span class="sxs-lookup"><span data-stu-id="de72b-103">AuxKlibQueryModuleInformation function</span></span>

<span data-ttu-id="de72b-104">Recupera le informazioni sul set di moduli attualmente caricato per il sistema.</span><span class="sxs-lookup"><span data-stu-id="de72b-104">Retrieves information about the currently loaded set of modules for the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="de72b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de72b-105">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a><span data-ttu-id="de72b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de72b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de72b-107">*BufferSize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="de72b-107">*BufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de72b-108">In input, dimensione del buffer *QueryInfo* in byte.</span><span class="sxs-lookup"><span data-stu-id="de72b-108">On input, the size of the *QueryInfo* buffer, in bytes.</span></span> <span data-ttu-id="de72b-109">Nell'output, riceve le dimensioni effettive richieste.</span><span class="sxs-lookup"><span data-stu-id="de72b-109">On output, receives the actual required size.</span></span> <span data-ttu-id="de72b-110">Poiché l'elenco dei moduli di sistema può variare tra le chiamate, questo valore può anche variare tra le chiamate.</span><span class="sxs-lookup"><span data-stu-id="de72b-110">Because the system module list can change between calls, this value can also change between calls.</span></span>

</dd> <dt>

<span data-ttu-id="de72b-111">*ElementSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de72b-111">*ElementSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de72b-112">Dimensione, in byte, di un elemento di matrice.</span><span class="sxs-lookup"><span data-stu-id="de72b-112">The size, in bytes, of an array element.</span></span> <span data-ttu-id="de72b-113">Questa dimensione determina il formato dell'output.</span><span class="sxs-lookup"><span data-stu-id="de72b-113">This size determines the format of the output.</span></span>

</dd> <dt>

<span data-ttu-id="de72b-114">*QueryInfo* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="de72b-114">*QueryInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="de72b-115">Puntatore a un buffer che riceve le informazioni sul modulo.</span><span class="sxs-lookup"><span data-stu-id="de72b-115">A pointer to a buffer that receives the module information.</span></span> <span data-ttu-id="de72b-116">Queste informazioni vengono restituite in una matrice i cui elementi sono una delle seguenti strutture: [**aux \_ module \_ Basic \_ info**](aux-module-basic-info-struct.md) o [**aux \_ module \_ Extended \_ info**](aux-module-extended-info-struct.md).</span><span class="sxs-lookup"><span data-stu-id="de72b-116">This information is returned in an array whose elements are one of the following structures: [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) or [**AUX\_MODULE\_EXTENDED\_INFO**](aux-module-extended-info-struct.md).</span></span> <span data-ttu-id="de72b-117">La struttura specifica utilizzata dipende dalla dimensione dell'elemento specificata.</span><span class="sxs-lookup"><span data-stu-id="de72b-117">The specific structure used depends on the specified element size.</span></span>

<span data-ttu-id="de72b-118">Se questo parametro è **null**, la funzione restituisce la dimensione del buffer richiesta.</span><span class="sxs-lookup"><span data-stu-id="de72b-118">If this parameter is **NULL**, the function returns the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de72b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de72b-119">Return value</span></span>

<span data-ttu-id="de72b-120">Se la funzione ha esito positivo, il valore restituito è STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="de72b-120">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="de72b-121">Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di stato definiti in ntstatus. h, disponibile in WDK.</span><span class="sxs-lookup"><span data-stu-id="de72b-121">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="de72b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="de72b-122">Remarks</span></span>

<span data-ttu-id="de72b-123">Prima di chiamare questa funzione, è necessario chiamare la funzione [**AuxKlibInitialize**](auxklibinitialize-func.md) .</span><span class="sxs-lookup"><span data-stu-id="de72b-123">You must call the [**AuxKlibInitialize**](auxklibinitialize-func.md) function before calling this function.</span></span>

<span data-ttu-id="de72b-124">La libreria di oggetti che implementa questa API può essere scaricata da [qui](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="de72b-124">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="de72b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de72b-125">Requirements</span></span>



| <span data-ttu-id="de72b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de72b-126">Requirement</span></span> | <span data-ttu-id="de72b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="de72b-127">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de72b-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="de72b-128">Redistributable</span></span><br/> | <span data-ttu-id="de72b-129">Libreria API ausiliaria Windows versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="de72b-129">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="de72b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de72b-130">Header</span></span><br/>          | <dl> <span data-ttu-id="de72b-131"><dt>Aux \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="de72b-131"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="de72b-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="de72b-132">Library</span></span><br/>         | <dl> <span data-ttu-id="de72b-133"><dt>Aux \_ klib. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de72b-133"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de72b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de72b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de72b-135">**AuxKlibInitialize**</span><span class="sxs-lookup"><span data-stu-id="de72b-135">**AuxKlibInitialize**</span></span>](auxklibinitialize-func.md)
</dt> <dt>

[<span data-ttu-id="de72b-136">**\_informazioni di \_ base sul modulo aux \_**</span><span class="sxs-lookup"><span data-stu-id="de72b-136">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> <dt>

[<span data-ttu-id="de72b-137">**\_ \_ informazioni estese sul modulo aux \_**</span><span class="sxs-lookup"><span data-stu-id="de72b-137">**AUX\_MODULE\_EXTENDED\_INFO**</span></span>](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




