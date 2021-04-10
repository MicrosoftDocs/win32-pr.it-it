---
description: La funzione MergeBlob copia tutte le voci dal BLOB di origine in un BLOB di destinazione.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Funzione MergeBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966772"
---
# <a name="mergeblob-function"></a><span data-ttu-id="4421f-103">MergeBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="4421f-103">MergeBlob function</span></span>

<span data-ttu-id="4421f-104">La funzione **MergeBlob** copia tutte le voci dal BLOB di origine in un BLOB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4421f-104">The **MergeBlob** function copies all of the entries from the source BLOB into a destination BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="4421f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4421f-105">Syntax</span></span>


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a><span data-ttu-id="4421f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4421f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4421f-107">*hDstBlob* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4421f-107">*hDstBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4421f-108">Handle per il BLOB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4421f-108">Handle to the destination BLOB.</span></span> <span data-ttu-id="4421f-109">In input, questo BLOB contiene le informazioni originali.</span><span class="sxs-lookup"><span data-stu-id="4421f-109">On input, this BLOB contains its original information.</span></span> <span data-ttu-id="4421f-110">Nell'output questo BLOB contiene le informazioni originali e tutte le informazioni del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="4421f-110">On output, this BLOB contains its original information plus all the information of the source BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="4421f-111">*hSrcBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4421f-111">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4421f-112">Handle per il BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="4421f-112">Handle to the source BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4421f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4421f-113">Return value</span></span>

<span data-ttu-id="4421f-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4421f-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4421f-115">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="4421f-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4421f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4421f-116">Remarks</span></span>

<span data-ttu-id="4421f-117">Le voci comuni ai file di origine e di destinazione verranno sovrascritte con i dati del BLOB di origine.</span><span class="sxs-lookup"><span data-stu-id="4421f-117">Entries common to source and destination files will be overwritten with data from the source BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="4421f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4421f-118">Requirements</span></span>



| <span data-ttu-id="4421f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4421f-119">Requirement</span></span> | <span data-ttu-id="4421f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4421f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4421f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4421f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4421f-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4421f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4421f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4421f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4421f-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4421f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4421f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4421f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4421f-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4421f-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="4421f-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="4421f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="4421f-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4421f-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="4421f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4421f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4421f-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4421f-130"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




