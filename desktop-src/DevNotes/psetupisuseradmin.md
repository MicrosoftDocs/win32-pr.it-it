---
description: Indica se l'utente corrente è un amministratore.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: pSetupIsUserAdmin (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330861"
---
# <a name="psetupisuseradmin-function"></a><span data-ttu-id="0f503-103">pSetupIsUserAdmin (funzione)</span><span class="sxs-lookup"><span data-stu-id="0f503-103">pSetupIsUserAdmin function</span></span>

<span data-ttu-id="0f503-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="0f503-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="0f503-105">Indica se l'utente corrente è un amministratore.</span><span class="sxs-lookup"><span data-stu-id="0f503-105">Indicates whether the current user is an administrator.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f503-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f503-106">Syntax</span></span>


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a><span data-ttu-id="0f503-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f503-107">Parameters</span></span>

<span data-ttu-id="0f503-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="0f503-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f503-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f503-109">Return value</span></span>

<span data-ttu-id="0f503-110">**True** se l'utente corrente è un amministratore; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0f503-110">**TRUE** if the current user is an administrator, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f503-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f503-111">Remarks</span></span>

<span data-ttu-id="0f503-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0f503-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f503-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f503-113">Requirements</span></span>



| <span data-ttu-id="0f503-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f503-114">Requirement</span></span> | <span data-ttu-id="0f503-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0f503-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f503-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0f503-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0f503-117"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f503-117"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
