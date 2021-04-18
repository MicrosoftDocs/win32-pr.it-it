---
description: Recupera lo stile del colore del testo dello stile specificato.
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: PColorStyleTextFromIMEStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 791fdaca4a93b0a44099306b8ae14ae4d5cb11cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330423"
---
# <a name="pcolorstyletextfromimestyle-function"></a><span data-ttu-id="cd57b-103">PColorStyleTextFromIMEStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="cd57b-103">PColorStyleTextFromIMEStyle function</span></span>

<span data-ttu-id="cd57b-104">Recupera lo stile del colore del testo dello stile specificato.</span><span class="sxs-lookup"><span data-stu-id="cd57b-104">Retrieves the text color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd57b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd57b-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="cd57b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd57b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd57b-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd57b-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd57b-108">Struttura **IMESTYLE** restituita dalla funzione [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="cd57b-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd57b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd57b-109">Return value</span></span>

<span data-ttu-id="cd57b-110">Puntatore a una struttura **IMECOLORSTY** che rappresenta lo stile del colore del testo.</span><span class="sxs-lookup"><span data-stu-id="cd57b-110">Pointer to an **IMECOLORSTY** structure representing the text color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd57b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd57b-111">Remarks</span></span>

<span data-ttu-id="cd57b-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="cd57b-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="cd57b-113">La struttura **IMECOLORSTY** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="cd57b-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a><span data-ttu-id="cd57b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd57b-114">Requirements</span></span>



| <span data-ttu-id="cd57b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd57b-115">Requirement</span></span> | <span data-ttu-id="cd57b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cd57b-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd57b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="cd57b-117">DLL</span></span><br/> | <dl> <span data-ttu-id="cd57b-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd57b-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd57b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd57b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd57b-120">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="cd57b-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
