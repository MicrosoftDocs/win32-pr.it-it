---
title: GetTextExtentPoint32Wrap (funzione)
description: Calcola la larghezza e l'altezza della stringa di testo specificata. Questa funzione esegue il wrapping di una chiamata a GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Controlli Windows per la funzione GetTextExtentPoint32Wrap
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740111"
---
# <a name="gettextextentpoint32wrap-function"></a><span data-ttu-id="e7609-105">GetTextExtentPoint32Wrap (funzione)</span><span class="sxs-lookup"><span data-stu-id="e7609-105">GetTextExtentPoint32Wrap function</span></span>

<span data-ttu-id="e7609-106">\[**GetTextExtentPoint32Wrap** è disponibile tramite Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="e7609-106">\[**GetTextExtentPoint32Wrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="e7609-107">Potrebbe essere modificato o non disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e7609-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e7609-108">Si consiglia invece di usare direttamente [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) .\]</span><span class="sxs-lookup"><span data-stu-id="e7609-108">It is recommended to use [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directly instead.\]</span></span>

<span data-ttu-id="e7609-109">Calcola la larghezza e l'altezza della stringa di testo specificata.</span><span class="sxs-lookup"><span data-stu-id="e7609-109">Computes the width and height of the specified string of text.</span></span> <span data-ttu-id="e7609-110">Questa funzione esegue il wrapping di una chiamata a [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="e7609-110">This function wraps a call to [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7609-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7609-111">Syntax</span></span>


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a><span data-ttu-id="e7609-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7609-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7609-113">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7609-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7609-114">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e7609-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e7609-115">Handle per il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7609-115">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="e7609-116">*lpString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7609-116">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7609-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e7609-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e7609-118">Puntatore a un buffer contenente il testo da disegnare.</span><span class="sxs-lookup"><span data-stu-id="e7609-118">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="e7609-119">La stringa non deve essere con terminazione zero, poiché *cbCount* specifica la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="e7609-119">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="e7609-120">*cbCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7609-120">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7609-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e7609-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e7609-122">Lunghezza, in byte, della stringa a cui punta *lpString*.</span><span class="sxs-lookup"><span data-stu-id="e7609-122">The length, in bytes, of the string pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="e7609-123">*lpSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e7609-123">*lpSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7609-124">Tipo: **LPSIZE**</span><span class="sxs-lookup"><span data-stu-id="e7609-124">Type: **LPSIZE**</span></span>

<span data-ttu-id="e7609-125">Quando termina, questo metodo contiene un puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) che contiene le dimensioni della stringa, in unità logiche.</span><span class="sxs-lookup"><span data-stu-id="e7609-125">When this method returns, contains a pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure containing the dimensions of the string, in logical units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7609-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7609-126">Return value</span></span>

<span data-ttu-id="e7609-127">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e7609-127">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e7609-128">Restituisce un valore diverso da zero se ha esito positivo; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="e7609-128">Returns a nonzero value if successful; otherwise, 0.</span></span>

<span data-ttu-id="e7609-129">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="e7609-129">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7609-130">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e7609-130">Remarks</span></span>

<span data-ttu-id="e7609-131">**GetTextExtentPoint32Wrap** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="e7609-131">**GetTextExtentPoint32Wrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="e7609-132">Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 420 da ComCtl32.dll per ottenere un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="e7609-132">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 420 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="e7609-133">Per ulteriori osservazioni, vedere [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="e7609-133">For additional remarks, please see [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7609-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7609-134">Requirements</span></span>



| <span data-ttu-id="e7609-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7609-135">Requirement</span></span> | <span data-ttu-id="e7609-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e7609-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7609-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7609-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e7609-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7609-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="e7609-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7609-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e7609-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7609-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e7609-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e7609-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7609-142"><dt>Comctl32.dll (versione 5,81 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e7609-142"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

