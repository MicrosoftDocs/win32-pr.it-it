---
description: Sposta un file o una directory esistente, inclusi i relativi elementi figlio.
ms.assetid: 1c533b02-6674-4390-bc49-6420403778a8
title: Funzione _MoveFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MoveFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 44c57d562feff62e21c4c769bfc9d6a650f4984c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324804"
---
# <a name="_movefile-function"></a><span data-ttu-id="cb726-103">\_MoveFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb726-103">\_MoveFile function</span></span>

<span data-ttu-id="cb726-104">\[Questa funzione è un wrapper per la funzione **MoveFile** .</span><span class="sxs-lookup"><span data-stu-id="cb726-104">\[This function is a wrapper over the **MoveFile** function.</span></span> <span data-ttu-id="cb726-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="cb726-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="cb726-106">Le applicazioni devono chiamare direttamente **MoveFile** .\]</span><span class="sxs-lookup"><span data-stu-id="cb726-106">Applications should call **MoveFile** directly.\]</span></span>

<span data-ttu-id="cb726-107">Sposta un file o una directory esistente, inclusi i relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="cb726-107">Moves an existing file or directory, including its children.</span></span> <span data-ttu-id="cb726-108">Vedere [ **MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span><span class="sxs-lookup"><span data-stu-id="cb726-108">See [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb726-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb726-109">Syntax</span></span>


```C++
BOOL _MoveFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="cb726-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb726-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb726-111">*...*</span><span class="sxs-lookup"><span data-stu-id="cb726-111">*...*</span></span> 
<span data-ttu-id="cb726-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cb726-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="cb726-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb726-113">Requirements</span></span>



| <span data-ttu-id="cb726-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb726-114">Requirement</span></span> | <span data-ttu-id="cb726-115">Valore</span><span class="sxs-lookup"><span data-stu-id="cb726-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb726-116">DLL</span><span class="sxs-lookup"><span data-stu-id="cb726-116">DLL</span></span><br/> | <dl> <span data-ttu-id="cb726-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb726-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb726-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb726-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb726-119">**MoveFile**</span><span class="sxs-lookup"><span data-stu-id="cb726-119">**MoveFile**</span></span>](/windows/win32/api/winbase/nf-winbase-movefile)
</dt> </dl>

 

 
