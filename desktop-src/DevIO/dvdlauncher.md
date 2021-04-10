---
description: Verifica che l'area multimediale nell'unità DVD corrisponda all'area dell'unità DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127291"
---
# <a name="dvdlauncher-function"></a><span data-ttu-id="53f02-103">DvdLauncher (funzione)</span><span class="sxs-lookup"><span data-stu-id="53f02-103">DvdLauncher function</span></span>

<span data-ttu-id="53f02-104">Verifica che l'area multimediale nell'unità DVD corrisponda all'area dell'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="53f02-104">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f02-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53f02-105">Syntax</span></span>


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="53f02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53f02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f02-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f02-107">*HWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f02-108">Handle per la finestra di primo livello da utilizzare per qualsiasi interfaccia utente richiesta.</span><span class="sxs-lookup"><span data-stu-id="53f02-108">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="53f02-109">*LetteraUnità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f02-109">*DriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f02-110">Lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="53f02-110">The drive letter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f02-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53f02-111">Return value</span></span>

<span data-ttu-id="53f02-112">Se la funzione ha esito positivo e le aree corrispondono, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="53f02-112">If the function succeeds and the regions match, the return value is nonzero.</span></span> <span data-ttu-id="53f02-113">In caso contrario, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="53f02-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f02-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="53f02-114">Remarks</span></span>

<span data-ttu-id="53f02-115">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="53f02-115">This function has no associated import library.</span></span> <span data-ttu-id="53f02-116">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a StorProp.dll.</span><span class="sxs-lookup"><span data-stu-id="53f02-116">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to StorProp.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f02-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53f02-117">Requirements</span></span>



| <span data-ttu-id="53f02-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f02-118">Requirement</span></span> | <span data-ttu-id="53f02-119">Valore</span><span class="sxs-lookup"><span data-stu-id="53f02-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53f02-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53f02-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53f02-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="53f02-121">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="53f02-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53f02-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53f02-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53f02-123">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="53f02-124">DLL</span><span class="sxs-lookup"><span data-stu-id="53f02-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53f02-125"><dt>StorProp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f02-125"><dt>StorProp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f02-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53f02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f02-127">Funzioni di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="53f02-127">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

