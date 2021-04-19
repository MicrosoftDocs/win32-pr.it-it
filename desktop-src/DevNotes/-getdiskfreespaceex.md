---
description: Ottiene lo spazio libero su disco.
ms.assetid: 4b7f4938-9918-4625-b28d-faf22de56976
title: Funzione _GetDiskFreeSpaceEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetDiskFreeSpaceEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
ms.openlocfilehash: da4a8eefabf03f6330ac9c1f135482f27dd8aa18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331977"
---
# <a name="_getdiskfreespaceex-function"></a><span data-ttu-id="f3a14-103">\_GetDiskFreeSpaceEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="f3a14-103">\_GetDiskFreeSpaceEx function</span></span>

<span data-ttu-id="f3a14-104">\[Questa funzione è un wrapper per la funzione **GetDiskFreeSpaceEx** .</span><span class="sxs-lookup"><span data-stu-id="f3a14-104">\[This function is a wrapper over the **GetDiskFreeSpaceEx** function.</span></span> <span data-ttu-id="f3a14-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="f3a14-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="f3a14-106">Le applicazioni devono chiamare direttamente **GetDiskFreeSpaceEx** .\]</span><span class="sxs-lookup"><span data-stu-id="f3a14-106">Applications should call **GetDiskFreeSpaceEx** directly.\]</span></span>

<span data-ttu-id="f3a14-107">Ottiene lo spazio libero su disco.</span><span class="sxs-lookup"><span data-stu-id="f3a14-107">Gets the free disk space.</span></span> <span data-ttu-id="f3a14-108">Vedere [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span><span class="sxs-lookup"><span data-stu-id="f3a14-108">See [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a14-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3a14-109">Syntax</span></span>


```C++
BOOL _GetDiskFreeSpaceEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="f3a14-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3a14-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a14-111">*...*</span><span class="sxs-lookup"><span data-stu-id="f3a14-111">*...*</span></span> 
<span data-ttu-id="f3a14-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f3a14-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f3a14-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3a14-113">Requirements</span></span>



| <span data-ttu-id="f3a14-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3a14-114">Requirement</span></span> | <span data-ttu-id="f3a14-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f3a14-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a14-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a14-116">DLL</span></span><br/> | <dl> <span data-ttu-id="f3a14-117"><dt>Msmdun80.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a14-117"><dt>Msmdun80.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a14-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3a14-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a14-119">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="f3a14-119">**GetDiskFreeSpaceEx**</span></span>](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa)
</dt> </dl>

 

 
