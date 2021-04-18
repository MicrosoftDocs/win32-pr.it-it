---
description: Termina la condivisione IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: EndIMEShare (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324448"
---
# <a name="endimeshare-function"></a><span data-ttu-id="a17aa-103">EndIMEShare (funzione)</span><span class="sxs-lookup"><span data-stu-id="a17aa-103">EndIMEShare function</span></span>

<span data-ttu-id="a17aa-104">Termina la condivisione IME.</span><span class="sxs-lookup"><span data-stu-id="a17aa-104">Terminates IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="a17aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a17aa-105">Syntax</span></span>


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="a17aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a17aa-106">Parameters</span></span>

<span data-ttu-id="a17aa-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="a17aa-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a17aa-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a17aa-108">Return value</span></span>

<span data-ttu-id="a17aa-109">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a17aa-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a17aa-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a17aa-110">Remarks</span></span>

<span data-ttu-id="a17aa-111">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a17aa-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="a17aa-112">Questa funzione deve essere chiamata dopo la chiamata dell'ultima funzione di condivisione IME.</span><span class="sxs-lookup"><span data-stu-id="a17aa-112">This function should be called after the last IME Share function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="a17aa-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a17aa-113">Requirements</span></span>



| <span data-ttu-id="a17aa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a17aa-114">Requirement</span></span> | <span data-ttu-id="a17aa-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a17aa-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a17aa-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a17aa-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a17aa-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a17aa-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a17aa-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a17aa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a17aa-119">**FInitIMEShare**</span><span class="sxs-lookup"><span data-stu-id="a17aa-119">**FInitIMEShare**</span></span>](finitimeshare.md)
</dt> </dl>

 

 
