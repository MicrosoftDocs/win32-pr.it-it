---
title: DrawTextWrap (funzione)
description: Disegna il testo formattato nel rettangolo specificato. Formatta il testo in base al metodo specificato (espandendo le schede, giustificando i caratteri, suddividendo le righe e così via). Questa funzione esegue il wrapping di una chiamata a DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Controlli Windows per la funzione DrawTextWrap
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963811"
---
# <a name="drawtextwrap-function"></a><span data-ttu-id="b1708-106">DrawTextWrap (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1708-106">DrawTextWrap function</span></span>

<span data-ttu-id="b1708-107">\[**DrawTextWrap** è disponibile tramite Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="b1708-107">\[**DrawTextWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="b1708-108">Potrebbe essere modificato o non disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b1708-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b1708-109">Si consiglia invece di utilizzare direttamente [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .\]</span><span class="sxs-lookup"><span data-stu-id="b1708-109">It is recommended to use [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directly instead.\]</span></span>

<span data-ttu-id="b1708-110">Disegna il testo formattato nel rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="b1708-110">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="b1708-111">Formatta il testo in base al metodo specificato (espandendo le schede, giustificando i caratteri, suddividendo le righe e così via).</span><span class="sxs-lookup"><span data-stu-id="b1708-111">It formats the text according to the specified method (expanding tabs, justifying characters, breaking lines, and so on).</span></span> <span data-ttu-id="b1708-112">Questa funzione esegue il wrapping di una chiamata a [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="b1708-112">This function wraps a call to [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1708-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1708-113">Syntax</span></span>


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="b1708-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1708-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1708-115">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1708-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1708-116">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b1708-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b1708-117">Handle per il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1708-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="b1708-118">*lpString* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b1708-118">*lpString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1708-119">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b1708-119">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b1708-120">Puntatore a un buffer contenente il testo da creare.</span><span class="sxs-lookup"><span data-stu-id="b1708-120">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="b1708-121">Se il parametro *nCount* è-1, la stringa deve essere con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="b1708-121">If the *nCount* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="b1708-122">Se *UFormat* include DT \_ MODIFYSTRING, la funzione potrebbe aggiungere fino a quattro caratteri aggiuntivi a questa stringa.</span><span class="sxs-lookup"><span data-stu-id="b1708-122">If *uFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="b1708-123">Il buffer che contiene la stringa deve essere sufficientemente grande da contenere questi caratteri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="b1708-123">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="b1708-124">*nCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1708-124">*nCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1708-125">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b1708-125">Type: **int**</span></span>

<span data-ttu-id="b1708-126">Lunghezza della stringa a cui punta *lpString*.</span><span class="sxs-lookup"><span data-stu-id="b1708-126">The length of the string pointed to by *lpString*.</span></span> <span data-ttu-id="b1708-127">Se *nCount* è-1, viene utilizzato il parametro *lpString* come puntatore a una stringa con terminazione null e [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calcola automaticamente il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="b1708-127">If *nCount* is -1, then the *lpString* parameter is assumed to be a pointer to a null-terminated string and [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="b1708-128">*lpRect* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b1708-128">*lpRect* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1708-129">Tipo: **lpRect**</span><span class="sxs-lookup"><span data-stu-id="b1708-129">Type: **LPRECT**</span></span>

<span data-ttu-id="b1708-130">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo.</span><span class="sxs-lookup"><span data-stu-id="b1708-130">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="b1708-131">*UFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1708-131">*uFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1708-132">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b1708-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b1708-133">Opzioni di formattazione.</span><span class="sxs-lookup"><span data-stu-id="b1708-133">The formatting options.</span></span> <span data-ttu-id="b1708-134">Per un elenco completo di opzioni, vedere la documentazione relativa a [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="b1708-134">See the documentation for [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="b1708-135">*lpDTParams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1708-135">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1708-136">Tipo: **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="b1708-136">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="b1708-137">Puntatore a una struttura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) che specifica le opzioni di formattazione aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="b1708-137">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="b1708-138">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b1708-138">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1708-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1708-139">Return value</span></span>

<span data-ttu-id="b1708-140">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b1708-140">Type: **int**</span></span>

<span data-ttu-id="b1708-141">Se la funzione ha esito positivo, il valore restituito è l'altezza del testo in unità logiche.</span><span class="sxs-lookup"><span data-stu-id="b1708-141">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="b1708-142">Se si specifica **DT \_ vCenter** o **DT \_ Bottom** , il valore restituito è l'offset dal **primo** membro di *LPRC* alla fine del testo disegnato se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="b1708-142">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text If the function fails, the return value is zero.</span></span>

<span data-ttu-id="b1708-143">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="b1708-143">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="b1708-144">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b1708-144">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1708-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b1708-145">Remarks</span></span>

<span data-ttu-id="b1708-146">**DrawTextWrap** non viene esportato in base al nome o dichiarato in un'intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="b1708-146">**DrawTextWrap** is not exported by name or declared in a public header.</span></span> <span data-ttu-id="b1708-147">Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 415 da ComCtl32.dll per ottenere un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="b1708-147">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 415 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="b1708-148">Per ulteriori osservazioni, vedere [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="b1708-148">For additional remarks, please see [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1708-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1708-149">Requirements</span></span>



| <span data-ttu-id="b1708-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1708-150">Requirement</span></span> | <span data-ttu-id="b1708-151">Valore</span><span class="sxs-lookup"><span data-stu-id="b1708-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1708-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1708-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b1708-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1708-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="b1708-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1708-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b1708-155">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1708-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b1708-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b1708-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1708-157"><dt>Comctl32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b1708-157"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

