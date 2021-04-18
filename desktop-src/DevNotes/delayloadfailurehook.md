---
description: Restituisce l'indirizzo di una funzione di callback di errore di caricamento ritardato per la DLL e il processo specificati.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327456"
---
# <a name="delayloadfailurehook-function"></a><span data-ttu-id="7752a-103">DelayLoadFailureHook (funzione)</span><span class="sxs-lookup"><span data-stu-id="7752a-103">DelayLoadFailureHook function</span></span>

<span data-ttu-id="7752a-104">Restituisce l'indirizzo di una funzione di callback di errore di caricamento ritardato per la DLL e il processo specificati.</span><span class="sxs-lookup"><span data-stu-id="7752a-104">Returns the address of a delay-load failure callback function for the specified DLL and process.</span></span>

## <a name="syntax"></a><span data-ttu-id="7752a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7752a-105">Syntax</span></span>


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a><span data-ttu-id="7752a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7752a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7752a-107">*pszDllName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7752a-107">*pszDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7752a-108">Nome della DLL.</span><span class="sxs-lookup"><span data-stu-id="7752a-108">The name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="7752a-109">*pszProcName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7752a-109">*pszProcName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7752a-110">Nome del processo.</span><span class="sxs-lookup"><span data-stu-id="7752a-110">The name of the process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7752a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7752a-111">Return value</span></span>

<span data-ttu-id="7752a-112">Indirizzo della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="7752a-112">The address of the callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7752a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7752a-113">Requirements</span></span>



| <span data-ttu-id="7752a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7752a-114">Requirement</span></span> | <span data-ttu-id="7752a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7752a-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7752a-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="7752a-116">Library</span></span><br/> | <dl> <span data-ttu-id="7752a-117"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7752a-117"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7752a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="7752a-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="7752a-119"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7752a-119"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7752a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7752a-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="7752a-121">[Hook di errore](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="7752a-121">[Failure Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




