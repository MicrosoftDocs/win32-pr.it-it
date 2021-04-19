---
description: Specifica se il colore specificato è un colore di base.
ms.assetid: 9a06fadc-9b97-4f7d-9488-688b72d14bc5
title: FFundamentalIMEColorStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FFundamentalIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c7de1bf4ef84d159d673e1039ad6ea328153b216
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328694"
---
# <a name="ffundamentalimecolorstyle-function"></a><span data-ttu-id="a57fb-103">FFundamentalIMEColorStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="a57fb-103">FFundamentalIMEColorStyle function</span></span>

<span data-ttu-id="a57fb-104">Specifica se il colore specificato è un colore di base.</span><span class="sxs-lookup"><span data-stu-id="a57fb-104">Specifies whether the specified color is a fundamental color.</span></span>

## <a name="syntax"></a><span data-ttu-id="a57fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a57fb-105">Syntax</span></span>


```C++
BOOL __cdecl FFundamentalIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="a57fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a57fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a57fb-107">*pcolorstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a57fb-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a57fb-108">Struttura **IMECOLORSTY** restituita dalla funzione [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="a57fb-108">An **IMECOLORSTY** structure returned from the [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a57fb-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a57fb-109">Return value</span></span>

<span data-ttu-id="a57fb-110">Restituisce **true** quando il colore è un colore di base.</span><span class="sxs-lookup"><span data-stu-id="a57fb-110">Returns **TRUE** when the color is a fundamental color.</span></span>

## <a name="remarks"></a><span data-ttu-id="a57fb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a57fb-111">Remarks</span></span>

<span data-ttu-id="a57fb-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a57fb-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a57fb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a57fb-113">Requirements</span></span>



| <span data-ttu-id="a57fb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a57fb-114">Requirement</span></span> | <span data-ttu-id="a57fb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a57fb-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a57fb-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a57fb-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a57fb-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a57fb-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a57fb-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a57fb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57fb-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="a57fb-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="a57fb-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="a57fb-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
