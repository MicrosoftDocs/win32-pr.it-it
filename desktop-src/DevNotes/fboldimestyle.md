---
description: Specifica se uno stile non di colore ha lo stile in grassetto.
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: FBoldIMEStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331666"
---
# <a name="fboldimestyle-function"></a><span data-ttu-id="0eecb-103">FBoldIMEStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="0eecb-103">FBoldIMEStyle function</span></span>

<span data-ttu-id="0eecb-104">Specifica se uno stile non di colore ha lo stile in grassetto.</span><span class="sxs-lookup"><span data-stu-id="0eecb-104">Specifies whether a non-color style has the bold style.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eecb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0eecb-105">Syntax</span></span>


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="0eecb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0eecb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eecb-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0eecb-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eecb-108">Struttura **IMESTYLE** restituita dalla funzione [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="0eecb-108">An **IMESTYLE** structure returned from the [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eecb-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0eecb-109">Return value</span></span>

<span data-ttu-id="0eecb-110">**True** se lo stile ha lo stile grassetto.</span><span class="sxs-lookup"><span data-stu-id="0eecb-110">**TRUE** if the style has the bold style.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eecb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0eecb-111">Remarks</span></span>

<span data-ttu-id="0eecb-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0eecb-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eecb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0eecb-113">Requirements</span></span>



| <span data-ttu-id="0eecb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eecb-114">Requirement</span></span> | <span data-ttu-id="0eecb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0eecb-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0eecb-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0eecb-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0eecb-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0eecb-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eecb-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0eecb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eecb-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="0eecb-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
