---
description: La funzione ValidateBitmapInfoHeader verifica una struttura BITMAPINFOHEADER per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Funzione ValidateBitmapInfoHeader (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333300"
---
# <a name="validatebitmapinfoheader-function"></a><span data-ttu-id="b7c9d-103">ValidateBitmapInfoHeader (funzione)</span><span class="sxs-lookup"><span data-stu-id="b7c9d-103">ValidateBitmapInfoHeader function</span></span>

<span data-ttu-id="b7c9d-104">La `ValidateBitmapInfoHeader` funzione verifica una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-104">The `ValidateBitmapInfoHeader` function checks a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="b7c9d-105">Questa funzione non garantisce che la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) sia valida o che il codice che usa la struttura sia protetto.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-105">This function does not guarantee that the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b7c9d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7c9d-106">Syntax</span></span>


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="b7c9d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7c9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7c9d-108">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="b7c9d-108">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="b7c9d-109">Puntatore alla struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) da convalidare.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-109">Pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure to validate.</span></span>

</dd> <dt>

<span data-ttu-id="b7c9d-110">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="b7c9d-110">*cbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b7c9d-111">Dimensioni in byte del blocco di memoria che include la struttura.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-111">Size of the memory block that holds the structure, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7c9d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7c9d-112">Return value</span></span>

<span data-ttu-id="b7c9d-113">Restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-113">Returns a Boolean value.</span></span> <span data-ttu-id="b7c9d-114">Se il valore è **false**, la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) non è valida.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-114">If the value is **FALSE**, the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7c9d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7c9d-115">Remarks</span></span>

<span data-ttu-id="b7c9d-116">Questa funzione protegge gli errori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7c9d-116">This function guards against the following errors:</span></span>

-   <span data-ttu-id="b7c9d-117">Overflow aritmetico nelle dimensioni della struttura o di una struttura non valida.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-117">Arithmetic overflow in the structure size or an invalid structure size.</span></span>
-   <span data-ttu-id="b7c9d-118">Valore non valido per il membro **biClrUsed** .</span><span class="sxs-lookup"><span data-stu-id="b7c9d-118">Invalid value for the **biClrUsed** member.</span></span>
-   <span data-ttu-id="b7c9d-119">Overflow aritmetico nelle dimensioni dell'immagine (**biSizeImage**).</span><span class="sxs-lookup"><span data-stu-id="b7c9d-119">Arithmetic overflow in the image size (**biSizeImage**).</span></span>
-   <span data-ttu-id="b7c9d-120">Valori non validi per la dimensione dell'immagine (**biSizeImage**) per i formati RGB.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-120">Invalid values for the image size (**biSizeImage**) for RGB formats.</span></span>

<span data-ttu-id="b7c9d-121">La funzione non controlla se la struttura descrive un formato video valido.</span><span class="sxs-lookup"><span data-stu-id="b7c9d-121">The function does not check whether the structure describes a valid video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c9d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7c9d-122">Requirements</span></span>



| <span data-ttu-id="b7c9d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7c9d-123">Requirement</span></span> | <span data-ttu-id="b7c9d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b7c9d-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c9d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7c9d-125">Header</span></span><br/> | <dl> <span data-ttu-id="b7c9d-126"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c9d-126"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c9d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7c9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c9d-128">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="b7c9d-128">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




