---
description: La funzione ThunkConnect32 viene usata dai driver di dispositivo a 16 bit (per MS-DOS) che effettuano chiamate nel kernel a 32 bit.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324859"
---
# <a name="thunkconnect32-function"></a><span data-ttu-id="5b173-103">ThunkConnect32 (funzione)</span><span class="sxs-lookup"><span data-stu-id="5b173-103">ThunkConnect32 function</span></span>

<span data-ttu-id="5b173-104">\[Questa funzione è supportata per compatibilità con le versioni precedenti, ma non è presente nelle versioni correnti di Windows.</span><span class="sxs-lookup"><span data-stu-id="5b173-104">\[This function was supported for backward compatibility, but is not present in current versions of Windows.</span></span> <span data-ttu-id="5b173-105">I nuovi driver di dispositivo dovrebbero essere 32 o 64 bit e non richiedono questa funzione.\]</span><span class="sxs-lookup"><span data-stu-id="5b173-105">New device drivers should be 32- or 64-bit and do not need this function.\]</span></span>

<span data-ttu-id="5b173-106">La funzione **ThunkConnect32** viene usata dai driver di dispositivo a 16 bit (per MS-DOS) che effettuano chiamate nel kernel a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5b173-106">The **ThunkConnect32** function is used by 16-bit device drivers (for MS-DOS) that call into the 32-bit kernel.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b173-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b173-107">Syntax</span></span>


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a><span data-ttu-id="5b173-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b173-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b173-109">*lpThunkData32*</span><span class="sxs-lookup"><span data-stu-id="5b173-109">*lpThunkData32*</span></span> 
</dt> <dd>

<span data-ttu-id="5b173-110">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="5b173-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b173-111">*pszThunkData16Name*</span><span class="sxs-lookup"><span data-stu-id="5b173-111">*pszThunkData16Name*</span></span> 
</dt> <dd>

<span data-ttu-id="5b173-112">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="5b173-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b173-113">*pszDll16*</span><span class="sxs-lookup"><span data-stu-id="5b173-113">*pszDll16*</span></span> 
</dt> <dd>

<span data-ttu-id="5b173-114">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="5b173-114">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b173-115">*pszDll32*</span><span class="sxs-lookup"><span data-stu-id="5b173-115">*pszDll32*</span></span> 
</dt> <dd>

<span data-ttu-id="5b173-116">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="5b173-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b173-117">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="5b173-117">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5b173-118">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="5b173-118">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b173-119">*dwReason*</span><span class="sxs-lookup"><span data-stu-id="5b173-119">*dwReason*</span></span> 
</dt> <dd>

<span data-ttu-id="5b173-120">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="5b173-120">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b173-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b173-121">Return value</span></span>

<span data-ttu-id="5b173-122">Restituisce sempre **false**.</span><span class="sxs-lookup"><span data-stu-id="5b173-122">Always returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b173-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b173-123">Requirements</span></span>



| <span data-ttu-id="5b173-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b173-124">Requirement</span></span> | <span data-ttu-id="5b173-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5b173-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b173-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5b173-126">DLL</span></span><br/> | <dl> <span data-ttu-id="5b173-127"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b173-127"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




