---
description: Specifica se il colore specificato è un colore del testo speciale.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: FSpecialTextIMEColorStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326580"
---
# <a name="fspecialtextimecolorstyle-function"></a><span data-ttu-id="94997-103">FSpecialTextIMEColorStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="94997-103">FSpecialTextIMEColorStyle function</span></span>

<span data-ttu-id="94997-104">Specifica se il colore specificato è un colore del testo speciale.</span><span class="sxs-lookup"><span data-stu-id="94997-104">Specifies whether the specified color is a special text color.</span></span>

## <a name="syntax"></a><span data-ttu-id="94997-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94997-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="94997-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94997-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94997-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94997-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94997-108">Struttura **IMECOLORSTY** restituita da una funzione [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="94997-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94997-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94997-109">Return value</span></span>

<span data-ttu-id="94997-110">Restituisce **true** quando il colore è un colore del testo speciale.</span><span class="sxs-lookup"><span data-stu-id="94997-110">Returns **TRUE** when the color is a special text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="94997-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="94997-111">Remarks</span></span>

<span data-ttu-id="94997-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="94997-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="94997-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94997-113">Requirements</span></span>



| <span data-ttu-id="94997-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="94997-114">Requirement</span></span> | <span data-ttu-id="94997-115">Valore</span><span class="sxs-lookup"><span data-stu-id="94997-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94997-116">DLL</span><span class="sxs-lookup"><span data-stu-id="94997-116">DLL</span></span><br/> | <dl> <span data-ttu-id="94997-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94997-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94997-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94997-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94997-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="94997-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="94997-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="94997-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
