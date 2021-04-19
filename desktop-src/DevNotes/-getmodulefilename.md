---
description: Ottiene il percorso del modulo.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: Funzione _GetModuleFileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331976"
---
# <a name="_getmodulefilename-function"></a><span data-ttu-id="3d197-103">\_GetModuleFileName (funzione)</span><span class="sxs-lookup"><span data-stu-id="3d197-103">\_GetModuleFileName function</span></span>

<span data-ttu-id="3d197-104">\[Questa funzione è un wrapper per la funzione **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="3d197-104">\[This function is a wrapper over the **GetModuleFileName** function.</span></span> <span data-ttu-id="3d197-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="3d197-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="3d197-106">Le applicazioni devono chiamare direttamente **GetModuleFileName** .\]</span><span class="sxs-lookup"><span data-stu-id="3d197-106">Applications should call **GetModuleFileName** directly.\]</span></span>

<span data-ttu-id="3d197-107">Ottiene il percorso del modulo.</span><span class="sxs-lookup"><span data-stu-id="3d197-107">Gets the module path.</span></span> <span data-ttu-id="3d197-108">Vedere [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span><span class="sxs-lookup"><span data-stu-id="3d197-108">See [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d197-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d197-109">Syntax</span></span>


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="3d197-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d197-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d197-111">*...*</span><span class="sxs-lookup"><span data-stu-id="3d197-111">*...*</span></span> 
<span data-ttu-id="3d197-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3d197-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3d197-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d197-113">Requirements</span></span>



| <span data-ttu-id="3d197-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d197-114">Requirement</span></span> | <span data-ttu-id="3d197-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3d197-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d197-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3d197-116">DLL</span></span><br/> | <dl> <span data-ttu-id="3d197-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d197-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d197-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d197-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d197-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="3d197-119">**GetModuleFileName**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
