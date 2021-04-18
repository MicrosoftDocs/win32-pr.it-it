---
description: Specifica se il colore specificato è un colore RGB.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: FRGBIMEColorStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: df11a2ad972791eaf7049bdef5fa927aaa4119da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328277"
---
# <a name="frgbimecolorstyle-function"></a><span data-ttu-id="856a7-103">FRGBIMEColorStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="856a7-103">FRGBIMEColorStyle function</span></span>

<span data-ttu-id="856a7-104">Specifica se il colore specificato è un colore RGB.</span><span class="sxs-lookup"><span data-stu-id="856a7-104">Specifies whether the specified color is an RGB color.</span></span>

## <a name="syntax"></a><span data-ttu-id="856a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="856a7-105">Syntax</span></span>


```C++
BOOL __cdecl FRGBIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="856a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="856a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="856a7-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="856a7-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="856a7-108">Struttura **IMECOLORSTY** restituita da una funzione [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="856a7-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="856a7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="856a7-109">Return value</span></span>

<span data-ttu-id="856a7-110">Restituisce **true** quando il colore è un colore RGB.</span><span class="sxs-lookup"><span data-stu-id="856a7-110">Returns **TRUE** when the color is an RGB color.</span></span>

## <a name="remarks"></a><span data-ttu-id="856a7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="856a7-111">Remarks</span></span>

<span data-ttu-id="856a7-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="856a7-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="856a7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="856a7-113">Requirements</span></span>



| <span data-ttu-id="856a7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="856a7-114">Requirement</span></span> | <span data-ttu-id="856a7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="856a7-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="856a7-116">DLL</span><span class="sxs-lookup"><span data-stu-id="856a7-116">DLL</span></span><br/> | <dl> <span data-ttu-id="856a7-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="856a7-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="856a7-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="856a7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856a7-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="856a7-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="856a7-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="856a7-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
