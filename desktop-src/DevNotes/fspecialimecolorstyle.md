---
description: Specifica se il colore specificato è un colore speciale.
ms.assetid: fda856c4-37b9-444f-9c54-d9eb848a4b05
title: FSpecialIMEColorStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: af6edf14f4c2167a4609cd8cbb671e85e297368d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326581"
---
# <a name="fspecialimecolorstyle-function"></a><span data-ttu-id="52123-103">FSpecialIMEColorStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="52123-103">FSpecialIMEColorStyle function</span></span>

<span data-ttu-id="52123-104">Specifica se il colore specificato è un colore speciale.</span><span class="sxs-lookup"><span data-stu-id="52123-104">Specifies whether the specified color is a special color.</span></span>

## <a name="syntax"></a><span data-ttu-id="52123-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52123-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="52123-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52123-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52123-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52123-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52123-108">Struttura **IMECOLORSTY** restituita da una funzione [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="52123-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52123-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52123-109">Return value</span></span>

<span data-ttu-id="52123-110">Restituisce **true** quando il colore è un colore speciale.</span><span class="sxs-lookup"><span data-stu-id="52123-110">Returns **TRUE** when the color is a special color.</span></span>

## <a name="remarks"></a><span data-ttu-id="52123-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="52123-111">Remarks</span></span>

<span data-ttu-id="52123-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="52123-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="52123-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52123-113">Requirements</span></span>



| <span data-ttu-id="52123-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52123-114">Requirement</span></span> | <span data-ttu-id="52123-115">Valore</span><span class="sxs-lookup"><span data-stu-id="52123-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52123-116">DLL</span><span class="sxs-lookup"><span data-stu-id="52123-116">DLL</span></span><br/> | <dl> <span data-ttu-id="52123-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52123-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52123-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52123-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52123-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="52123-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="52123-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="52123-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
