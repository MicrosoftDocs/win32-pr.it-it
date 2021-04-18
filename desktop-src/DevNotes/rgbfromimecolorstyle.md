---
description: Converte una struttura IMECOLORSTY in una struttura COLORREF.
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: RGBFromIMEColorStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7993253e5e11c45cae3e062467db080201bc1228
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324863"
---
# <a name="rgbfromimecolorstyle-function"></a><span data-ttu-id="6d877-103">RGBFromIMEColorStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="6d877-103">RGBFromIMEColorStyle function</span></span>

<span data-ttu-id="6d877-104">Converte una struttura **IMECOLORSTY** in una struttura [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="6d877-104">Converts an **IMECOLORSTY** structure to a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d877-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d877-105">Syntax</span></span>


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="6d877-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d877-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d877-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d877-108">Struttura **IMECOLORSTY** restituita da una funzione [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="6d877-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d877-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d877-109">Return value</span></span>

<span data-ttu-id="6d877-110">Restituisce una struttura [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="6d877-110">Returns a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d877-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d877-111">Remarks</span></span>

<span data-ttu-id="6d877-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6d877-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d877-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d877-113">Requirements</span></span>



| <span data-ttu-id="6d877-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d877-114">Requirement</span></span> | <span data-ttu-id="6d877-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6d877-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d877-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6d877-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6d877-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d877-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d877-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d877-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d877-119">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="6d877-119">**COLORREF**</span></span>](../gdi/colorref.md)
</dt> <dt>

[<span data-ttu-id="6d877-120">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="6d877-120">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="6d877-121">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="6d877-121">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
