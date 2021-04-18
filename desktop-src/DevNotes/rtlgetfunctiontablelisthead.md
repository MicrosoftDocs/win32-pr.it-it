---
description: Consente a un debugger di esaminare le informazioni sulla tabella della funzione dinamica.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330959"
---
# <a name="rtlgetfunctiontablelisthead-function"></a><span data-ttu-id="96e1f-103">RtlGetFunctionTableListHead (funzione)</span><span class="sxs-lookup"><span data-stu-id="96e1f-103">RtlGetFunctionTableListHead function</span></span>

<span data-ttu-id="96e1f-104">\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]</span><span class="sxs-lookup"><span data-stu-id="96e1f-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="96e1f-105">Consente a un debugger di esaminare le informazioni sulla tabella della funzione dinamica.</span><span class="sxs-lookup"><span data-stu-id="96e1f-105">Enables a debugger to examine dynamic function table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e1f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96e1f-106">Syntax</span></span>


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a><span data-ttu-id="96e1f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="96e1f-107">Parameters</span></span>

<span data-ttu-id="96e1f-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="96e1f-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96e1f-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96e1f-109">Return value</span></span>

<span data-ttu-id="96e1f-110">Restituisce un puntatore all'inizio dell'elenco della tabella di funzioni.</span><span class="sxs-lookup"><span data-stu-id="96e1f-110">Returns a pointer to the head of the function table list.</span></span>

## <a name="remarks"></a><span data-ttu-id="96e1f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="96e1f-111">Remarks</span></span>

<span data-ttu-id="96e1f-112">Si noti che il file di intestazione di Windows Driver Kit (WDK) Ntdef. h è necessario per alcune definizioni.</span><span class="sxs-lookup"><span data-stu-id="96e1f-112">Note that the Windows Driver Kit (WDK) header file Ntdef.h is required for some definitions.</span></span> <span data-ttu-id="96e1f-113">La libreria di importazione associata, Ntdll. lib, è disponibile in WDK.</span><span class="sxs-lookup"><span data-stu-id="96e1f-113">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="96e1f-114">È anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire un collegamento dinamico a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="96e1f-114">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e1f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96e1f-115">Requirements</span></span>



| <span data-ttu-id="96e1f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="96e1f-116">Requirement</span></span> | <span data-ttu-id="96e1f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="96e1f-117">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96e1f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="96e1f-118">DLL</span></span><br/> | <dl> <span data-ttu-id="96e1f-119"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96e1f-119"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
