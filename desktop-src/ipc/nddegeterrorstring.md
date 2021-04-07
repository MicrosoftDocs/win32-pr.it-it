---
description: Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che descrive il codice di errore restituito.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Funzione NDdeGetErrorString (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049347"
---
# <a name="nddegeterrorstring-function"></a><span data-ttu-id="e891d-103">NDdeGetErrorString (funzione)</span><span class="sxs-lookup"><span data-stu-id="e891d-103">NDdeGetErrorString function</span></span>

<span data-ttu-id="e891d-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="e891d-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="e891d-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="e891d-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="e891d-106">Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che descrive il codice di errore restituito.</span><span class="sxs-lookup"><span data-stu-id="e891d-106">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e891d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e891d-107">Syntax</span></span>


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="e891d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e891d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e891d-109">*codice uerrorcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e891d-109">*uErrorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e891d-110">Codice di errore da convertire in una stringa di errore.</span><span class="sxs-lookup"><span data-stu-id="e891d-110">The error code to be converted into an error string.</span></span>

</dd> <dt>

<span data-ttu-id="e891d-111">*lpszErrorString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e891d-111">*lpszErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e891d-112">Puntatore a un buffer che riceve la stringa di errore tradotta.</span><span class="sxs-lookup"><span data-stu-id="e891d-112">A pointer to a buffer that receives the translated error string.</span></span> <span data-ttu-id="e891d-113">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e891d-113">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="e891d-114">Se il buffer non è sufficientemente grande da archiviare la stringa di errore completa, la stringa viene troncata.</span><span class="sxs-lookup"><span data-stu-id="e891d-114">If the buffer is not large enough to store the complete error string, the string is truncated.</span></span>

</dd> <dt>

<span data-ttu-id="e891d-115">*cBufSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e891d-115">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e891d-116">Dimensione del buffer in cui ricevere la stringa di errore, in **TCHARs**.</span><span class="sxs-lookup"><span data-stu-id="e891d-116">The size of the buffer to receive the error string, in **TCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e891d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e891d-117">Return value</span></span>

<span data-ttu-id="e891d-118">Se la funzione ha esito positivo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="e891d-118">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="e891d-119">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e891d-119">If the function fails, the return value is a nonzero error code.</span></span> <span data-ttu-id="e891d-120">Se il buffer *lpszErrorString* non è sufficientemente grande da accettare la stringa di errore completa e la stringa viene troncata, la funzione restituisce il valore \_ errore interno di NDDE \_ .</span><span class="sxs-lookup"><span data-stu-id="e891d-120">If the *lpszErrorString* buffer is not large enough to accept the complete error string, and the string is truncated, the function returns the value NDDE\_INTERNAL\_ERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="e891d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e891d-121">Requirements</span></span>



| <span data-ttu-id="e891d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e891d-122">Requirement</span></span> | <span data-ttu-id="e891d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e891d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e891d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e891d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e891d-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e891d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e891d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e891d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e891d-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e891d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e891d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e891d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e891d-129"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e891d-129"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="e891d-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="e891d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e891d-131"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e891d-131"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e891d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e891d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e891d-133"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e891d-133"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="e891d-134">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e891d-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e891d-135">**NDdeGetErrorStringW** (Unicode) e **NDdeGetErrorStringA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e891d-135">**NDdeGetErrorStringW** (Unicode) and **NDdeGetErrorStringA** (ANSI)</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e891d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e891d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e891d-137">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="e891d-137">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="e891d-138">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="e891d-138">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




