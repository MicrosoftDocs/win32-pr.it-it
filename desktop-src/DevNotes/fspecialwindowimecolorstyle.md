---
description: Specifica se il colore specificato è un colore della finestra speciale.
ms.assetid: 41f7d4fb-9718-42a8-89df-c29bd8c0665b
title: FSpecialWindowIMEColorStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialWindowIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fb667186789361a106a23f8daa82088b9bcb2ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326836"
---
# <a name="fspecialwindowimecolorstyle-function"></a><span data-ttu-id="a8c79-103">FSpecialWindowIMEColorStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="a8c79-103">FSpecialWindowIMEColorStyle function</span></span>

<span data-ttu-id="a8c79-104">Specifica se il colore specificato è un colore della finestra speciale.</span><span class="sxs-lookup"><span data-stu-id="a8c79-104">Specifies whether the specified color is a special window color.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8c79-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialWindowIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="a8c79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8c79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c79-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8c79-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c79-108">Struttura **IMECOLORSTY** restituita da una funzione [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c79-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8c79-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8c79-109">Return value</span></span>

<span data-ttu-id="a8c79-110">Restituisce **true** quando il colore è un colore speciale della finestra (uno dei colori speciali).</span><span class="sxs-lookup"><span data-stu-id="a8c79-110">Returns **TRUE** when the color is a special window color (one of special color).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8c79-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8c79-111">Remarks</span></span>

<span data-ttu-id="a8c79-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a8c79-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c79-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8c79-113">Requirements</span></span>



| <span data-ttu-id="a8c79-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8c79-114">Requirement</span></span> | <span data-ttu-id="a8c79-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a8c79-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c79-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a8c79-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a8c79-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8c79-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8c79-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8c79-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c79-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="a8c79-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="a8c79-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="a8c79-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
