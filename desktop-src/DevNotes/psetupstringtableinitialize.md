---
description: Inizializza una tabella di stringhe.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: pSetupStringTableInitialize (funzione)
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
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325204"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="13b54-103">pSetupStringTableInitialize (funzione)</span><span class="sxs-lookup"><span data-stu-id="13b54-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="13b54-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="13b54-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="13b54-105">Inizializza una tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="13b54-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b54-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13b54-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="13b54-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="13b54-107">Parameters</span></span>

<span data-ttu-id="13b54-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="13b54-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="13b54-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="13b54-109">Remarks</span></span>

<span data-ttu-id="13b54-110">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="13b54-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b54-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13b54-111">Requirements</span></span>



| <span data-ttu-id="13b54-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="13b54-112">Requirement</span></span> | <span data-ttu-id="13b54-113">Valore</span><span class="sxs-lookup"><span data-stu-id="13b54-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13b54-114">DLL</span><span class="sxs-lookup"><span data-stu-id="13b54-114">DLL</span></span><br/> | <dl> <span data-ttu-id="13b54-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b54-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
