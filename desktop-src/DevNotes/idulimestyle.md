---
description: Indica se lo stile non colore specificato presenta sottolineatura.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: IdUlIMEStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330964"
---
# <a name="idulimestyle-function"></a><span data-ttu-id="efbdd-103">IdUlIMEStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="efbdd-103">IdUlIMEStyle function</span></span>

<span data-ttu-id="efbdd-104">Indica se lo stile non colore specificato presenta sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="efbdd-104">Identifies whether the specified non-color style has underline.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbdd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efbdd-105">Syntax</span></span>


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="efbdd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="efbdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efbdd-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efbdd-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efbdd-108">Struttura **IMESTYLE** restituita dalla funzione [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="efbdd-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efbdd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efbdd-109">Return value</span></span>

<span data-ttu-id="efbdd-110">Questa funzione può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="efbdd-110">This function can returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="efbdd-111">**IMESTY \_ UL \_ min** (2002)</span><span class="sxs-lookup"><span data-stu-id="efbdd-111">**IMESTY\_UL\_MIN** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-112">**IMESTY \_ UL \_ None** (2002)</span><span class="sxs-lookup"><span data-stu-id="efbdd-112">**IMESTY\_UL\_NONE** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-113">**IMESTY \_ UL \_ singolo** (2003)</span><span class="sxs-lookup"><span data-stu-id="efbdd-113">**IMESTY\_UL\_SINGLE** (2003)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-114">**IMESTY \_ UL \_ punteggiato** (2005)</span><span class="sxs-lookup"><span data-stu-id="efbdd-114">**IMESTY\_UL\_DOTTED** (2005)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-115">**IMESTY \_ \_Spessore UL** (2006)</span><span class="sxs-lookup"><span data-stu-id="efbdd-115">**IMESTY\_UL\_THICK** (2006)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-116">**IMESTY \_ UL \_ inferiore** (2011)</span><span class="sxs-lookup"><span data-stu-id="efbdd-116">**IMESTY\_UL\_LOWER** (2011)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-117">**IMESTY \_ UL \_ THICKLOWER** (2012)</span><span class="sxs-lookup"><span data-stu-id="efbdd-117">**IMESTY\_UL\_THICKLOWER** (2012)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-118">**IMESTY \_ UL \_ THICKDITHLOWER** (2013)</span><span class="sxs-lookup"><span data-stu-id="efbdd-118">**IMESTY\_UL\_THICKDITHLOWER** (2013)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-119">**IMESTY \_ UL \_ DITHLOWER** (2014)</span><span class="sxs-lookup"><span data-stu-id="efbdd-119">**IMESTY\_UL\_DITHLOWER** (2014)</span></span>
</dt> <dt>

<span data-ttu-id="efbdd-120">**IMESTY \_ UL \_ Max** (2014)</span><span class="sxs-lookup"><span data-stu-id="efbdd-120">**IMESTY\_UL\_MAX** (2014)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="efbdd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="efbdd-121">Remarks</span></span>

<span data-ttu-id="efbdd-122">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="efbdd-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="efbdd-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efbdd-123">Requirements</span></span>



| <span data-ttu-id="efbdd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="efbdd-124">Requirement</span></span> | <span data-ttu-id="efbdd-125">Valore</span><span class="sxs-lookup"><span data-stu-id="efbdd-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efbdd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="efbdd-126">DLL</span></span><br/> | <dl> <span data-ttu-id="efbdd-127"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efbdd-127"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efbdd-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efbdd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbdd-129">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="efbdd-129">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
