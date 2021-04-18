---
description: Il metodo UpdateColourTable aggiorna la tabella dei colori con una nuova tavolozza.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Metodo CDrawImage. UpdateColourTable (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333718"
---
# <a name="cdrawimageupdatecolourtable-method"></a><span data-ttu-id="cad73-103">CDrawImage. UpdateColourTable, metodo</span><span class="sxs-lookup"><span data-stu-id="cad73-103">CDrawImage.UpdateColourTable method</span></span>

<span data-ttu-id="cad73-104">Il `UpdateColourTable` metodo aggiorna la tabella dei colori con una nuova tavolozza.</span><span class="sxs-lookup"><span data-stu-id="cad73-104">The `UpdateColourTable` method updates the color table with a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad73-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cad73-105">Syntax</span></span>


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a><span data-ttu-id="cad73-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cad73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cad73-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="cad73-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="cad73-108">Contesto di dispositivo che contiene l'immagine.</span><span class="sxs-lookup"><span data-stu-id="cad73-108">Device context containing the image.</span></span>

</dd> <dt>

<span data-ttu-id="cad73-109">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="cad73-109">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="cad73-110">Puntatore a una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) contenente la nuova tavolozza.</span><span class="sxs-lookup"><span data-stu-id="cad73-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure containing the new palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cad73-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cad73-111">Return value</span></span>

<span data-ttu-id="cad73-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cad73-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad73-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cad73-113">Requirements</span></span>



| <span data-ttu-id="cad73-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cad73-114">Requirement</span></span> | <span data-ttu-id="cad73-115">Valore</span><span class="sxs-lookup"><span data-stu-id="cad73-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cad73-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cad73-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cad73-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cad73-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cad73-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="cad73-118">Library</span></span><br/> | <dl> <span data-ttu-id="cad73-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cad73-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad73-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cad73-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad73-121">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="cad73-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




