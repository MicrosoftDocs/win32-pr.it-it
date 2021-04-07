---
title: BNS (objidl. h)
description: Un blocco di nome stringa (BNS) è un puntatore a una matrice di puntatori alle stringhe che termina con un puntatore NULL.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- BNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963992"
---
# <a name="snb"></a><span data-ttu-id="31114-104">BNS</span><span class="sxs-lookup"><span data-stu-id="31114-104">SNB</span></span>

<span data-ttu-id="31114-105">Un blocco di nome stringa (**BNS**) è un puntatore a una matrice di puntatori alle stringhe che termina con un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="31114-105">A string name block (**SNB**) is a pointer to an array of pointers to strings, that ends in a **NULL** pointer.</span></span> <span data-ttu-id="31114-106">I blocchi dei nomi di stringa vengono usati dall'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e dalle chiamate di funzione che aprono gli oggetti di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="31114-106">String name blocks are used by the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and by function calls that open storage objects.</span></span> <span data-ttu-id="31114-107">Le stringhe puntano a oggetti o flussi di archiviazione contenuti che devono essere esclusi nelle chiamate aperte.</span><span class="sxs-lookup"><span data-stu-id="31114-107">The strings point to contained storage objects or streams that are to be excluded in the open calls.</span></span>


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

<span data-ttu-id="31114-108">**BNS**</span><span class="sxs-lookup"><span data-stu-id="31114-108">**SNB**</span></span>
</dt> <dd>

<span data-ttu-id="31114-109">\[\_marshalling Wire (wireSNB)\]</span><span class="sxs-lookup"><span data-stu-id="31114-109">\[wire\_marshal(wireSNB)\]</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31114-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="31114-110">Remarks</span></span>

<span data-ttu-id="31114-111">È necessario creare la **BNS** allocando un blocco di memoria contiguo in cui i puntatori alle stringhe sono seguiti da un puntatore **null** , seguito dalle stringhe effettive.</span><span class="sxs-lookup"><span data-stu-id="31114-111">The **SNB** should be created by allocating a contiguous block of memory in which the pointers to strings are followed by a **NULL** pointer, which is then followed by the actual strings.</span></span>

<span data-ttu-id="31114-112">Il marshalling di un **BNS** si basa sul presupposto che la **BNS** passata è stata creata in questo modo.</span><span class="sxs-lookup"><span data-stu-id="31114-112">The marshaling of an **SNB** is based on the assumption that the **SNB** that was passed in was created in this way.</span></span> <span data-ttu-id="31114-113">Sebbene possa essere archiviato in altri modi, il **BNS** creato in questo modo presenta il vantaggio di richiedere solo un'operazione di allocazione e una libera memoria per tutte le stringhe.</span><span class="sxs-lookup"><span data-stu-id="31114-113">Although it could be stored in other ways, the **SNB** created in this manner has the advantage of requiring only one allocation operation and one freeing of memory for all the strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="31114-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31114-114">Requirements</span></span>



| <span data-ttu-id="31114-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="31114-115">Requirement</span></span> | <span data-ttu-id="31114-116">Valore</span><span class="sxs-lookup"><span data-stu-id="31114-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31114-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31114-117">Minimum supported client</span></span><br/> | <span data-ttu-id="31114-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="31114-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="31114-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31114-119">Minimum supported server</span></span><br/> | <span data-ttu-id="31114-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="31114-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="31114-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31114-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="31114-122"><dt>Objidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31114-122"><dt>Objidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="31114-123">IDL</span><span class="sxs-lookup"><span data-stu-id="31114-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31114-124"><dt>Objidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31114-124"><dt>Objidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31114-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31114-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31114-126">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="31114-126">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





