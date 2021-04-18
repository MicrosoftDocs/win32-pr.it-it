---
description: Carica una libreria.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: Funzione _LoadLibrary
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325684"
---
# <a name="_loadlibrary-function"></a><span data-ttu-id="386a0-103">\_LoadLibrary (funzione)</span><span class="sxs-lookup"><span data-stu-id="386a0-103">\_LoadLibrary function</span></span>

<span data-ttu-id="386a0-104">\[Questa funzione è un wrapper della funzione **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="386a0-104">\[This function is a wrapper over the **LoadLibrary** function.</span></span> <span data-ttu-id="386a0-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="386a0-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="386a0-106">Le applicazioni devono chiamare **LoadLibrary** direttamente.\]</span><span class="sxs-lookup"><span data-stu-id="386a0-106">Applications should call **LoadLibrary** directly.\]</span></span>

<span data-ttu-id="386a0-107">Carica una libreria.</span><span class="sxs-lookup"><span data-stu-id="386a0-107">Loads a library.</span></span> <span data-ttu-id="386a0-108">Vedere [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="386a0-108">See [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

## <a name="syntax"></a><span data-ttu-id="386a0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="386a0-109">Syntax</span></span>


```C++
HMODULE _LoadLibrary(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="386a0-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="386a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="386a0-111">*...*</span><span class="sxs-lookup"><span data-stu-id="386a0-111">*...*</span></span> 
<span data-ttu-id="386a0-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="386a0-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="386a0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="386a0-113">Requirements</span></span>



| <span data-ttu-id="386a0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="386a0-114">Requirement</span></span> | <span data-ttu-id="386a0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="386a0-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="386a0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="386a0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="386a0-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="386a0-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="386a0-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="386a0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386a0-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="386a0-119">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
