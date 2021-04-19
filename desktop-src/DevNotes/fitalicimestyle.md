---
description: Specifica se uno stile non colore presenta lo stile corsivo.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: FItalicIMEStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329980"
---
# <a name="fitalicimestyle-function"></a><span data-ttu-id="d80ad-103">FItalicIMEStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="d80ad-103">FItalicIMEStyle function</span></span>

<span data-ttu-id="d80ad-104">Specifica se uno stile non colore presenta lo stile corsivo.</span><span class="sxs-lookup"><span data-stu-id="d80ad-104">Specifies whether a non-color style has the italic style.</span></span>

## <a name="syntax"></a><span data-ttu-id="d80ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d80ad-105">Syntax</span></span>


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="d80ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d80ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d80ad-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d80ad-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d80ad-108">Struttura **IMESTYLE** restituita dalla funzione [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="d80ad-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d80ad-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d80ad-109">Return value</span></span>

<span data-ttu-id="d80ad-110">**True** se lo stile ha lo stile corsivo.</span><span class="sxs-lookup"><span data-stu-id="d80ad-110">**TRUE** if the style has the italic style.</span></span>

## <a name="remarks"></a><span data-ttu-id="d80ad-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d80ad-111">Remarks</span></span>

<span data-ttu-id="d80ad-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d80ad-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d80ad-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d80ad-113">Requirements</span></span>



| <span data-ttu-id="d80ad-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d80ad-114">Requirement</span></span> | <span data-ttu-id="d80ad-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d80ad-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d80ad-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d80ad-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d80ad-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d80ad-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d80ad-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d80ad-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d80ad-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="d80ad-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
