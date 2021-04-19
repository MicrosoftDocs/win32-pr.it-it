---
description: Ottiene un riferimento a un oggetto driver TCP V6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332367"
---
# <a name="referencetcpdriverv6-function"></a><span data-ttu-id="112d0-103">ReferenceTcpDriverV6 (funzione)</span><span class="sxs-lookup"><span data-stu-id="112d0-103">ReferenceTcpDriverV6 function</span></span>

<span data-ttu-id="112d0-104">Ottiene un riferimento a un oggetto driver TCP V6.</span><span class="sxs-lookup"><span data-stu-id="112d0-104">Obtains a reference to a TCP v6 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="112d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="112d0-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="112d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="112d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="112d0-107">*ppDriverObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="112d0-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="112d0-108">Puntatore a una struttura **di \_ oggetti driver** .</span><span class="sxs-lookup"><span data-stu-id="112d0-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="112d0-109">Per ulteriori informazioni, vedere la documentazione relativa a WDK.</span><span class="sxs-lookup"><span data-stu-id="112d0-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="112d0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="112d0-110">Return value</span></span>

<span data-ttu-id="112d0-111">Se la funzione ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="112d0-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="112d0-112">Se ha esito negativo, verrà restituito il codice di stato appropriato.</span><span class="sxs-lookup"><span data-stu-id="112d0-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="112d0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="112d0-113">Remarks</span></span>

<span data-ttu-id="112d0-114">Questa funzione può essere chiamata solo dalla modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="112d0-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="112d0-115">Il chiamante deve decrementare il conteggio dei riferimenti chiamando la funzione **ObDereferenceObject** al termine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="112d0-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="112d0-116">Questa funzione è implementata in Drvref. lib, disponibile per il download.</span><span class="sxs-lookup"><span data-stu-id="112d0-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="112d0-117">Vedere [libreria API di riferimento per il driver di rete Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="112d0-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="112d0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="112d0-118">Requirements</span></span>



| <span data-ttu-id="112d0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="112d0-119">Requirement</span></span> | <span data-ttu-id="112d0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="112d0-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="112d0-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="112d0-121">Library</span></span><br/> | <dl> <span data-ttu-id="112d0-122"><dt>Drvref. lib</dt></span><span class="sxs-lookup"><span data-stu-id="112d0-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="112d0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="112d0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112d0-124">**ReferenceTcpDriver**</span><span class="sxs-lookup"><span data-stu-id="112d0-124">**ReferenceTcpDriver**</span></span>](referencetcpdriver.md)
</dt> </dl>

 

 




