---
description: Recupera lo stile del colore di sfondo dello stile specificato.
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: PColorStyleBackFromIMEStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 33ff9072fc5e850654f932817cd4ecf0e9372aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328958"
---
# <a name="pcolorstylebackfromimestyle-function"></a><span data-ttu-id="caf1a-103">PColorStyleBackFromIMEStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="caf1a-103">PColorStyleBackFromIMEStyle function</span></span>

<span data-ttu-id="caf1a-104">Recupera lo stile del colore di sfondo dello stile specificato.</span><span class="sxs-lookup"><span data-stu-id="caf1a-104">Retrieves the background color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf1a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="caf1a-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="caf1a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="caf1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf1a-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="caf1a-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf1a-108">Struttura **IMESTYLE** restituita dalla funzione [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="caf1a-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caf1a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="caf1a-109">Return value</span></span>

<span data-ttu-id="caf1a-110">Puntatore a una struttura **IMECOLORSTY** che rappresenta lo stile del colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="caf1a-110">Pointer to an **IMECOLORSTY** structure representing the background color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="caf1a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="caf1a-111">Remarks</span></span>

<span data-ttu-id="caf1a-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="caf1a-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="caf1a-113">La struttura **IMECOLORSTY** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="caf1a-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="caf1a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="caf1a-114">Requirements</span></span>



| <span data-ttu-id="caf1a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="caf1a-115">Requirement</span></span> | <span data-ttu-id="caf1a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="caf1a-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="caf1a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="caf1a-117">DLL</span></span><br/> | <dl> <span data-ttu-id="caf1a-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caf1a-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caf1a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="caf1a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf1a-120">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="caf1a-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
