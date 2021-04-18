---
description: Determina se un nome di condivisione utilizza la sintassi corretta.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Funzione NDdeIsValidShareName (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305712"
---
# <a name="nddeisvalidsharename-function"></a><span data-ttu-id="c4039-103">NDdeIsValidShareName (funzione)</span><span class="sxs-lookup"><span data-stu-id="c4039-103">NDdeIsValidShareName function</span></span>

<span data-ttu-id="c4039-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="c4039-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="c4039-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="c4039-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="c4039-106">Determina se un nome di condivisione utilizza la sintassi corretta.</span><span class="sxs-lookup"><span data-stu-id="c4039-106">Determines whether a share name uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4039-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4039-107">Syntax</span></span>


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a><span data-ttu-id="c4039-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4039-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4039-109">*ShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4039-109">*shareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4039-110">Nome della condivisione da convalidare.</span><span class="sxs-lookup"><span data-stu-id="c4039-110">The share name to be validated.</span></span> <span data-ttu-id="c4039-111">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c4039-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4039-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4039-112">Return value</span></span>

<span data-ttu-id="c4039-113">Se il nome della condivisione ha una sintassi valida, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c4039-113">If the share name has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="c4039-114">Se il nome della condivisione non ha una sintassi valida, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="c4039-114">If the share name does not have valid syntax, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4039-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4039-115">Remarks</span></span>

<span data-ttu-id="c4039-116">Questa funzione viene chiamata anche da [**NDDEShareAdd**](nddeshareadd.md) quando crea la condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="c4039-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4039-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4039-117">Requirements</span></span>



| <span data-ttu-id="c4039-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4039-118">Requirement</span></span> | <span data-ttu-id="c4039-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c4039-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4039-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4039-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c4039-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c4039-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c4039-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4039-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c4039-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c4039-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4039-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4039-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4039-125"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4039-125"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4039-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4039-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4039-127"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4039-127"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c4039-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c4039-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4039-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4039-129"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4039-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c4039-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c4039-131">**NDdeIsValidShareNameW** (Unicode) e **NDdeIsValidShareNameA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c4039-131">**NDdeIsValidShareNameW** (Unicode) and **NDdeIsValidShareNameA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="c4039-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4039-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4039-133">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="c4039-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="c4039-134">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="c4039-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="c4039-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="c4039-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




