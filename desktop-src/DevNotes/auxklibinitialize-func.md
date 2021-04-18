---
description: Inizializza la \_ libreria aux klib.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Funzione AuxKlibInitialize (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331973"
---
# <a name="auxklibinitialize-function"></a><span data-ttu-id="5e161-103">AuxKlibInitialize (funzione)</span><span class="sxs-lookup"><span data-stu-id="5e161-103">AuxKlibInitialize function</span></span>

<span data-ttu-id="5e161-104">Inizializza la \_ libreria aux klib.</span><span class="sxs-lookup"><span data-stu-id="5e161-104">Initializes the Aux\_klib library.</span></span> <span data-ttu-id="5e161-105">Questa funzione deve essere chiamata prima che sia possibile chiamare qualsiasi altra funzione nella libreria.</span><span class="sxs-lookup"><span data-stu-id="5e161-105">This function must be called before any other function in the library can be called.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e161-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e161-106">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="5e161-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e161-107">Parameters</span></span>

<span data-ttu-id="5e161-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="5e161-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e161-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e161-109">Return value</span></span>

<span data-ttu-id="5e161-110">Se la funzione ha esito positivo, il valore restituito è STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5e161-110">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="5e161-111">Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di stato definiti in ntstatus. h, disponibile in WDK.</span><span class="sxs-lookup"><span data-stu-id="5e161-111">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e161-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e161-112">Remarks</span></span>

<span data-ttu-id="5e161-113">La libreria di oggetti che implementa questa API può essere scaricata da [qui](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="5e161-113">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e161-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e161-114">Requirements</span></span>



| <span data-ttu-id="5e161-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e161-115">Requirement</span></span> | <span data-ttu-id="5e161-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5e161-116">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e161-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5e161-117">Redistributable</span></span><br/> | <span data-ttu-id="5e161-118">Libreria API ausiliaria Windows versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="5e161-118">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="5e161-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e161-119">Header</span></span><br/>          | <dl> <span data-ttu-id="5e161-120"><dt>Aux \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e161-120"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e161-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e161-121">Library</span></span><br/>         | <dl> <span data-ttu-id="5e161-122"><dt>Aux \_ klib. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e161-122"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e161-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e161-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e161-124">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="5e161-124">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




