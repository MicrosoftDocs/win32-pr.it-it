---
description: Specifica se uno stile non di colore ha uno stile di sottolineatura.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: FUlIMEStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: a49090d2ca192dfd3ec6d0064b92bd2233af79c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326835"
---
# <a name="fulimestyle-function"></a><span data-ttu-id="8da83-103">FUlIMEStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="8da83-103">FUlIMEStyle function</span></span>

<span data-ttu-id="8da83-104">Specifica se uno stile non di colore ha uno stile di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="8da83-104">Specifies whether a non-color style has an underline style.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8da83-105">Syntax</span></span>


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="8da83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8da83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da83-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8da83-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da83-108">Struttura **IMESTYLE** restituita dalla funzione [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="8da83-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8da83-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8da83-109">Return value</span></span>

<span data-ttu-id="8da83-110">TRUE se lo stile ha uno stile di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="8da83-110">TRUE if the style has an underline style.</span></span>

## <a name="remarks"></a><span data-ttu-id="8da83-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8da83-111">Remarks</span></span>

<span data-ttu-id="8da83-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8da83-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8da83-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8da83-113">Requirements</span></span>



| <span data-ttu-id="8da83-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da83-114">Requirement</span></span> | <span data-ttu-id="8da83-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8da83-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8da83-116">DLL</span><span class="sxs-lookup"><span data-stu-id="8da83-116">DLL</span></span><br/> | <dl> <span data-ttu-id="8da83-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8da83-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da83-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8da83-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da83-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="8da83-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
