---
description: Ottiene un riferimento a un oggetto driver TCP V4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: ReferenceTcpDriver (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332658"
---
# <a name="referencetcpdriver-function"></a><span data-ttu-id="ec93d-103">ReferenceTcpDriver (funzione)</span><span class="sxs-lookup"><span data-stu-id="ec93d-103">ReferenceTcpDriver function</span></span>

<span data-ttu-id="ec93d-104">Ottiene un riferimento a un oggetto driver TCP V4.</span><span class="sxs-lookup"><span data-stu-id="ec93d-104">Obtains a reference to a TCP v4 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec93d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec93d-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="ec93d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec93d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec93d-107">*ppDriverObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ec93d-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec93d-108">Puntatore a una struttura **di \_ oggetti driver** .</span><span class="sxs-lookup"><span data-stu-id="ec93d-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="ec93d-109">Per ulteriori informazioni, vedere la documentazione relativa a WDK.</span><span class="sxs-lookup"><span data-stu-id="ec93d-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec93d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec93d-110">Return value</span></span>

<span data-ttu-id="ec93d-111">Se la funzione ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="ec93d-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="ec93d-112">Se ha esito negativo, verrà restituito il codice di stato appropriato.</span><span class="sxs-lookup"><span data-stu-id="ec93d-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec93d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec93d-113">Remarks</span></span>

<span data-ttu-id="ec93d-114">Questa funzione può essere chiamata solo dalla modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="ec93d-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="ec93d-115">Il chiamante deve decrementare il conteggio dei riferimenti chiamando la funzione **ObDereferenceObject** al termine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec93d-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="ec93d-116">Questa funzione è implementata in Drvref. lib, disponibile per il download.</span><span class="sxs-lookup"><span data-stu-id="ec93d-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="ec93d-117">Vedere [libreria API di riferimento per il driver di rete Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="ec93d-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec93d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec93d-118">Requirements</span></span>



| <span data-ttu-id="ec93d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec93d-119">Requirement</span></span> | <span data-ttu-id="ec93d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ec93d-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec93d-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec93d-121">Library</span></span><br/> | <dl> <span data-ttu-id="ec93d-122"><dt>Drvref. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec93d-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec93d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec93d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec93d-124">**ReferenceTcpDriverV6**</span><span class="sxs-lookup"><span data-stu-id="ec93d-124">**ReferenceTcpDriverV6**</span></span>](referencetcpdriverv6.md)
</dt> </dl>

 

 




