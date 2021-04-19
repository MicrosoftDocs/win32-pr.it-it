---
description: Inizializza la condivisione IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: FInitIMEShare (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329981"
---
# <a name="finitimeshare-function"></a><span data-ttu-id="60556-103">FInitIMEShare (funzione)</span><span class="sxs-lookup"><span data-stu-id="60556-103">FInitIMEShare function</span></span>

<span data-ttu-id="60556-104">Inizializza la condivisione IME.</span><span class="sxs-lookup"><span data-stu-id="60556-104">Initializes IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="60556-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60556-105">Syntax</span></span>


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="60556-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60556-106">Parameters</span></span>

<span data-ttu-id="60556-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="60556-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60556-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60556-108">Return value</span></span>

<span data-ttu-id="60556-109">La funzione restituisce **true** in caso di esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="60556-109">The function returns **TRUE** on success or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="60556-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="60556-110">Remarks</span></span>

<span data-ttu-id="60556-111">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="60556-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="60556-112">Questa funzione deve essere chiamata prima che vengano chiamate altre funzioni di condivisione IME.</span><span class="sxs-lookup"><span data-stu-id="60556-112">This function should be called before any other IME Share functions are called.</span></span>

## <a name="requirements"></a><span data-ttu-id="60556-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60556-113">Requirements</span></span>



| <span data-ttu-id="60556-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="60556-114">Requirement</span></span> | <span data-ttu-id="60556-115">Valore</span><span class="sxs-lookup"><span data-stu-id="60556-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60556-116">DLL</span><span class="sxs-lookup"><span data-stu-id="60556-116">DLL</span></span><br/> | <dl> <span data-ttu-id="60556-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60556-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60556-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60556-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60556-119">**EndIMEShare**</span><span class="sxs-lookup"><span data-stu-id="60556-119">**EndIMEShare**</span></span>](endimeshare.md)
</dt> </dl>

 

 
