---
title: ExtTextOutWrap (funzione)
description: Disegna il testo usando il tipo di carattere, il colore di sfondo e il colore del testo attualmente selezionati. Facoltativamente, è possibile specificare le dimensioni da utilizzare per il ritaglio, l'opacità o entrambi. Questa funzione esegue il wrapping di una chiamata a ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Controlli Windows per la funzione ExtTextOutWrap
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119083"
---
# <a name="exttextoutwrap-function"></a><span data-ttu-id="1511c-106">ExtTextOutWrap (funzione)</span><span class="sxs-lookup"><span data-stu-id="1511c-106">ExtTextOutWrap function</span></span>

<span data-ttu-id="1511c-107">\[**ExtTextOutWrap** è disponibile tramite Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="1511c-107">\[**ExtTextOutWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="1511c-108">Potrebbe essere modificato o non disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1511c-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1511c-109">Si consiglia invece di usare direttamente [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .\]</span><span class="sxs-lookup"><span data-stu-id="1511c-109">It is recommended to use [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directly instead.\]</span></span>

<span data-ttu-id="1511c-110">Disegna il testo usando il tipo di carattere, il colore di sfondo e il colore del testo attualmente selezionati.</span><span class="sxs-lookup"><span data-stu-id="1511c-110">Draws text using the currently selected font, background color, and text color.</span></span> <span data-ttu-id="1511c-111">Facoltativamente, è possibile specificare le dimensioni da utilizzare per il ritaglio, l'opacità o entrambi.</span><span class="sxs-lookup"><span data-stu-id="1511c-111">You can optionally provide dimensions to be used for clipping, opacity, or both.</span></span> <span data-ttu-id="1511c-112">Questa funzione esegue il wrapping di una chiamata a [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="1511c-112">This function wraps a call to [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="syntax"></a><span data-ttu-id="1511c-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1511c-113">Syntax</span></span>


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a><span data-ttu-id="1511c-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="1511c-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1511c-115">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1511c-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1511c-116">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1511c-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1511c-117">Handle per il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1511c-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="1511c-118">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1511c-118">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1511c-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1511c-119">Type: **int**</span></span>

<span data-ttu-id="1511c-120">Coordinata x, in coordinate logiche, del punto di riferimento utilizzato per posizionare la stringa.</span><span class="sxs-lookup"><span data-stu-id="1511c-120">The x-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="1511c-121">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1511c-121">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1511c-122">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1511c-122">Type: **int**</span></span>

<span data-ttu-id="1511c-123">Coordinata y, in coordinate logiche, del punto di riferimento utilizzato per posizionare la stringa.</span><span class="sxs-lookup"><span data-stu-id="1511c-123">The y-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="1511c-124">*uOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1511c-124">*uOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1511c-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1511c-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1511c-126">Valori che specificano come usare il rettangolo definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1511c-126">Values that specify how to use the application-defined rectangle.</span></span> <span data-ttu-id="1511c-127">Per un elenco completo delle opzioni, vedere [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .</span><span class="sxs-lookup"><span data-stu-id="1511c-127">See [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="1511c-128">*LPRC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1511c-128">*lprc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1511c-129">Tipo: \**const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="1511c-129">Type: \**const [**RECT**](/previous-versions//dd162897(v=vs.85))\** _</span></span>

<span data-ttu-id="1511c-130">Puntatore a una struttura facoltativa [_ *Rect* \*](/previous-versions//dd162897(v=vs.85)) che specifica le dimensioni, in coordinate logiche, di un rettangolo utilizzato per il ritaglio, l'opacità o entrambi.</span><span class="sxs-lookup"><span data-stu-id="1511c-130">A pointer to an optional [_ *RECT*\*](/previous-versions//dd162897(v=vs.85)) structure that specifies the dimensions, in logical coordinates, of a rectangle that is used for clipping, opacity, or both.</span></span>

</dd> <dt>

<span data-ttu-id="1511c-131">*lpString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1511c-131">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1511c-132">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1511c-132">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1511c-133">Puntatore a un buffer contenente il testo da disegnare.</span><span class="sxs-lookup"><span data-stu-id="1511c-133">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="1511c-134">La stringa non deve essere con terminazione zero, poiché *cbCount* specifica la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="1511c-134">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="1511c-135">*cbCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1511c-135">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1511c-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1511c-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1511c-137">Lunghezza della stringa, in byte, a cui punta *lpString*.</span><span class="sxs-lookup"><span data-stu-id="1511c-137">The length of the string, in bytes, pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="1511c-138">*lpDx* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1511c-138">*lpDx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1511c-139">Tipo: \**const [**int**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="1511c-139">Type: \**const [**INT**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="1511c-140">Puntatore a una matrice di valori facoltativa che indica la distanza tra le origini delle celle di caratteri adiacenti.</span><span class="sxs-lookup"><span data-stu-id="1511c-140">A pointer to an optional array of values that indicate the distance between origins of adjacent character cells.</span></span> <span data-ttu-id="1511c-141">Ad esempio, \[ \] le unità logiche _lpDx \* x separano le origini della cella di tipo carattere x e della cella (x + 1).</span><span class="sxs-lookup"><span data-stu-id="1511c-141">For example, _lpDx\*\[x\] logical units separate the origins of character cell x and character cell (x + 1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1511c-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1511c-142">Return value</span></span>

<span data-ttu-id="1511c-143">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1511c-143">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1511c-144">Restituisce un valore diverso da zero se la stringa viene disegnata correttamente.</span><span class="sxs-lookup"><span data-stu-id="1511c-144">Returns a nonzero value if the string is drawn successfully.</span></span> <span data-ttu-id="1511c-145">Tuttavia, se la versione ANSI di [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) viene chiamata con l' \_ indice del glifo Eto \_ , la funzione restituisce **true** anche se la funzione non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="1511c-145">However, if the ANSI version of [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) is called with ETO\_GLYPH\_INDEX, the function returns **TRUE** even though the function does nothing.</span></span>

<span data-ttu-id="1511c-146">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="1511c-146">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="1511c-147">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="1511c-147">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="1511c-148">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1511c-148">Remarks</span></span>

<span data-ttu-id="1511c-149">**ExtTextOutWrap** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="1511c-149">**ExtTextOutWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="1511c-150">Per usarlo, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 417 da ComCtl32.dll per ottenere un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="1511c-150">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 417 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="1511c-151">Per ulteriori osservazioni, vedere [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="1511c-151">For additional remarks, please see [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="requirements"></a><span data-ttu-id="1511c-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1511c-152">Requirements</span></span>



| <span data-ttu-id="1511c-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="1511c-153">Requirement</span></span> | <span data-ttu-id="1511c-154">Valore</span><span class="sxs-lookup"><span data-stu-id="1511c-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1511c-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1511c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="1511c-156">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1511c-156">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="1511c-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1511c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="1511c-158">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1511c-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1511c-159">DLL</span><span class="sxs-lookup"><span data-stu-id="1511c-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1511c-160"><dt>Comctl32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="1511c-160"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

