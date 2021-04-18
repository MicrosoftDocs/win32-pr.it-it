---
description: Ottiene il nome del computer.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: Funzione _GetComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328097"
---
# <a name="_getcomputername-function"></a><span data-ttu-id="b1c9b-103">\_GetComputerName (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1c9b-103">\_GetComputerName function</span></span>

<span data-ttu-id="b1c9b-104">\[Questa funzione è un wrapper della funzione **GetComputerName** .</span><span class="sxs-lookup"><span data-stu-id="b1c9b-104">\[This function is a wrapper over the **GetComputerName** function.</span></span> <span data-ttu-id="b1c9b-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="b1c9b-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="b1c9b-106">Le applicazioni devono chiamare direttamente **GetComputerName** .\]</span><span class="sxs-lookup"><span data-stu-id="b1c9b-106">Applications should call **GetComputerName** directly.\]</span></span>

<span data-ttu-id="b1c9b-107">Ottiene il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="b1c9b-107">Gets the computer name.</span></span> <span data-ttu-id="b1c9b-108">Vedere [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span><span class="sxs-lookup"><span data-stu-id="b1c9b-108">See [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1c9b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1c9b-109">Syntax</span></span>


```C++
BOOL _GetComputerName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="b1c9b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1c9b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1c9b-111">*...*</span><span class="sxs-lookup"><span data-stu-id="b1c9b-111">*...*</span></span> 
<span data-ttu-id="b1c9b-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b1c9b-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b1c9b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1c9b-113">Requirements</span></span>



| <span data-ttu-id="b1c9b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1c9b-114">Requirement</span></span> | <span data-ttu-id="b1c9b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b1c9b-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c9b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="b1c9b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="b1c9b-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1c9b-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1c9b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1c9b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1c9b-119">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="b1c9b-119">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
