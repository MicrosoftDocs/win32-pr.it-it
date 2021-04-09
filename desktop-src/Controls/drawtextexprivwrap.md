---
title: DrawTextExPrivWrap (funzione)
description: Disegna il testo formattato nel rettangolo specificato. Questa funzione esegue il wrapping di una chiamata a DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Controlli Windows per la funzione DrawTextExPrivWrap
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964941"
---
# <a name="drawtextexprivwrap-function"></a><span data-ttu-id="ab9ca-105">DrawTextExPrivWrap (funzione)</span><span class="sxs-lookup"><span data-stu-id="ab9ca-105">DrawTextExPrivWrap function</span></span>

<span data-ttu-id="ab9ca-106">\[**DrawTextExPrivWrap** è disponibile tramite Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="ab9ca-106">\[**DrawTextExPrivWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="ab9ca-107">Potrebbe essere modificato o non disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ab9ca-108">Si consiglia invece di usare direttamente [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-108">It is recommended to use [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directly instead.\]</span></span>

<span data-ttu-id="ab9ca-109">Disegna il testo formattato nel rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-109">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="ab9ca-110">Questa funzione esegue il wrapping di una chiamata a [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="ab9ca-110">This function wraps a call to [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab9ca-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab9ca-111">Syntax</span></span>


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="ab9ca-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab9ca-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab9ca-113">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9ca-114">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ab9ca-115">Handle per il contesto di dispositivo in cui eseguire il progetto.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-115">A handle to the device context in which to draw.</span></span>

</dd> <dt>

<span data-ttu-id="ab9ca-116">*lpchText* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-116">*lpchText* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9ca-117">Tipo: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-117">Type: **[**LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ab9ca-118">Puntatore a un buffer contenente il testo da creare.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-118">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="ab9ca-119">Se il parametro *cchText* è-1, la stringa deve essere con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-119">If the *cchText* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="ab9ca-120">Se *dwDTFormat* include DT \_ MODIFYSTRING, la funzione potrebbe aggiungere fino a quattro caratteri aggiuntivi a questa stringa.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-120">If *dwDTFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="ab9ca-121">Il buffer che contiene la stringa deve essere sufficientemente grande da contenere questi caratteri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-121">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="ab9ca-122">*cchText* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-122">*cchText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9ca-123">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-123">Type: **int**</span></span>

<span data-ttu-id="ab9ca-124">Lunghezza della stringa a cui punta *lpchText*.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-124">The length of the string pointed to by *lpchText*.</span></span> <span data-ttu-id="ab9ca-125">Se *cchText* è-1, si presuppone che il parametro *lpchText* sia un puntatore a una stringa con terminazione null e [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calcoli automaticamente il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-125">If *cchText* is -1, then the *lpchText* parameter is assumed to be a pointer to a null-terminated string and [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="ab9ca-126">*LPRC* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-126">*lprc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9ca-127">Tipo: **lpRect**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-127">Type: **LPRECT**</span></span>

<span data-ttu-id="ab9ca-128">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-128">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="ab9ca-129">*dwDTFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-129">*dwDTFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9ca-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ab9ca-131">Opzioni di formattazione.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-131">The formatting options.</span></span> <span data-ttu-id="ab9ca-132">Per un elenco completo delle opzioni, vedere la documentazione relativa a [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .</span><span class="sxs-lookup"><span data-stu-id="ab9ca-132">See the documentation for [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="ab9ca-133">*lpDTParams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-133">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9ca-134">Tipo: **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-134">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="ab9ca-135">Puntatore a una struttura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) che specifica le opzioni di formattazione aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-135">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="ab9ca-136">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-136">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab9ca-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab9ca-137">Return value</span></span>

<span data-ttu-id="ab9ca-138">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-138">Type: **int**</span></span>

<span data-ttu-id="ab9ca-139">Se la funzione ha esito positivo, il valore restituito è l'altezza del testo in unità logiche.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-139">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="ab9ca-140">Se si specifica **DT \_ vCenter** o **DT \_ Bottom** , il valore restituito è l'offset dal **primo** membro di *LPRC* alla fine del testo disegnato.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-140">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text.</span></span>

<span data-ttu-id="ab9ca-141">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-141">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="ab9ca-142">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ab9ca-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab9ca-143">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ab9ca-143">Remarks</span></span>

<span data-ttu-id="ab9ca-144">**DrawTextExPrivWrap** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-144">**DrawTextExPrivWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="ab9ca-145">Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 416 da ComCtl32.dll per ottenere un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-145">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 416 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="ab9ca-146">Per ulteriori osservazioni, vedere [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="ab9ca-146">For additional remarks, please see [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab9ca-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab9ca-147">Requirements</span></span>



| <span data-ttu-id="ab9ca-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab9ca-148">Requirement</span></span> | <span data-ttu-id="ab9ca-149">Valore</span><span class="sxs-lookup"><span data-stu-id="ab9ca-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9ca-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab9ca-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ab9ca-151">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-151">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="ab9ca-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab9ca-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ab9ca-153">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab9ca-154">DLL</span><span class="sxs-lookup"><span data-stu-id="ab9ca-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab9ca-155"><dt>Comctl32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ca-155"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

