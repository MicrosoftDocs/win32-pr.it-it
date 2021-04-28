---
description: 'Funzione pSetupStringTableInitialize: inizializza una tabella di stringhe.'
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: Funzione pSetupStringTableInitialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 79638f9f1f80f4b9b3d54a33c7e94234174ffb19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089200"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="89416-103">Funzione pSetupStringTableInitialize</span><span class="sxs-lookup"><span data-stu-id="89416-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="89416-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="89416-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="89416-105">Inizializza una tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="89416-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="89416-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89416-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="89416-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="89416-107">Parameters</span></span>

<span data-ttu-id="89416-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="89416-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="89416-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="89416-109">Remarks</span></span>

<span data-ttu-id="89416-110">A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)</span><span class="sxs-lookup"><span data-stu-id="89416-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="89416-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89416-111">Requirements</span></span>



| <span data-ttu-id="89416-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="89416-112">Requirement</span></span> | <span data-ttu-id="89416-113">Valore</span><span class="sxs-lookup"><span data-stu-id="89416-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89416-114">DLL</span><span class="sxs-lookup"><span data-stu-id="89416-114">DLL</span></span><br/> | <dl> <span data-ttu-id="89416-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89416-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
