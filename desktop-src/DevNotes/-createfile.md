---
description: Crea o apre un file.
ms.assetid: 2a993f45-7f87-4b9e-bccc-277477558d3c
title: Funzione _CreateFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _CreateFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: becd7fed9e32385409b78e00169191a12b550e3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326681"
---
# <a name="_createfile-function"></a><span data-ttu-id="4ab95-103">\_CreateFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="4ab95-103">\_CreateFile function</span></span>

<span data-ttu-id="4ab95-104">\[Questa funzione è un wrapper della funzione **CreateFile** .</span><span class="sxs-lookup"><span data-stu-id="4ab95-104">\[This function is a wrapper over the **CreateFile** function.</span></span> <span data-ttu-id="4ab95-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="4ab95-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="4ab95-106">Le applicazioni devono chiamare **CreateFile** direttamente.\]</span><span class="sxs-lookup"><span data-stu-id="4ab95-106">Applications should call **CreateFile** directly.\]</span></span>

<span data-ttu-id="4ab95-107">Crea o apre un file.</span><span class="sxs-lookup"><span data-stu-id="4ab95-107">Creates or opens a file.</span></span> <span data-ttu-id="4ab95-108">Vedere [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span><span class="sxs-lookup"><span data-stu-id="4ab95-108">See [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab95-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ab95-109">Syntax</span></span>


```C++
BOOL _CreateFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="4ab95-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ab95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ab95-111">*...*</span><span class="sxs-lookup"><span data-stu-id="4ab95-111">*...*</span></span> 
<span data-ttu-id="4ab95-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4ab95-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4ab95-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ab95-113">Requirements</span></span>



| <span data-ttu-id="4ab95-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ab95-114">Requirement</span></span> | <span data-ttu-id="4ab95-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab95-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab95-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4ab95-116">DLL</span></span><br/> | <dl> <span data-ttu-id="4ab95-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ab95-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ab95-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ab95-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab95-119">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="4ab95-119">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> </dl>

 

