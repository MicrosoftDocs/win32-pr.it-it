---
description: Crea una matrice di handle per le icone estratte da un file specificato.
title: SHExtractIconsW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: d82eb48d45210ebf12464708b09fe469d97432db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994805"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="7fe77-103">SHExtractIconsW (funzione)</span><span class="sxs-lookup"><span data-stu-id="7fe77-103">SHExtractIconsW function</span></span>

<span data-ttu-id="7fe77-104">\[**SHExtractIconsW** è disponibile tramite Windows XP Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="7fe77-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="7fe77-105">Potrebbe essere modificato o non disponibile nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="7fe77-106">Crea una matrice di handle per le icone estratte da un file specificato.</span><span class="sxs-lookup"><span data-stu-id="7fe77-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe77-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fe77-107">Syntax</span></span>


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a><span data-ttu-id="7fe77-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fe77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fe77-109">*pszFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe77-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7fe77-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="7fe77-111">Puntatore al nome file da cui estrarre le icone.</span><span class="sxs-lookup"><span data-stu-id="7fe77-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="7fe77-112">*nIconIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe77-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7fe77-113">Type: **int**</span></span>

<span data-ttu-id="7fe77-114">Indice della prima icona da estrarre dalla risorsa denominata in *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="7fe77-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="7fe77-115">*cxIcon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe77-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7fe77-116">Type: **int**</span></span>

<span data-ttu-id="7fe77-117">Larghezza desiderata dell'icona.</span><span class="sxs-lookup"><span data-stu-id="7fe77-117">The desired width of the icon.</span></span> <span data-ttu-id="7fe77-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7fe77-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7fe77-119">*cyIcon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe77-120">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7fe77-120">Type: **int**</span></span>

<span data-ttu-id="7fe77-121">Altezza desiderata dell'icona.</span><span class="sxs-lookup"><span data-stu-id="7fe77-121">The desired height of the icon.</span></span> <span data-ttu-id="7fe77-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7fe77-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7fe77-123">*phIcon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe77-124">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="7fe77-124">Type: \**HICON\** _</span></span>

<span data-ttu-id="7fe77-125">Quando la funzione restituisce un risultato, contiene un puntatore alla matrice di handle di icona.</span><span class="sxs-lookup"><span data-stu-id="7fe77-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="7fe77-126">_pIconId \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-126">_pIconId\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe77-127">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="7fe77-127">Type: \**UINT\** _</span></span>

<span data-ttu-id="7fe77-128">Quando la funzione restituisce un risultato, contiene un puntatore all'identificatore di risorsa dell'icona estratta che meglio si adatta al dispositivo di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="7fe77-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="7fe77-129">Se non è disponibile alcun identificatore per questo formato, contiene 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7fe77-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="7fe77-130">Se non è possibile ottenere un identificatore per qualsiasi altro motivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="7fe77-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="7fe77-131">_nIcons \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-131">_nIcons\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe77-132">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7fe77-132">Type: **UINT**</span></span>

<span data-ttu-id="7fe77-133">Il numero di icone da estrarre dalla risorsa denominata in *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="7fe77-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="7fe77-134">Questo parametro è valido solo se la risorsa è un file con estensione exe o dll.</span><span class="sxs-lookup"><span data-stu-id="7fe77-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="7fe77-135">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe77-136">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7fe77-136">Type: **UINT**</span></span>

<span data-ttu-id="7fe77-137">Flag che controllano questa funzione.</span><span class="sxs-lookup"><span data-stu-id="7fe77-137">The flags that control this function.</span></span> <span data-ttu-id="7fe77-138">Per i valori possibili, vedere il parametro *fuLoad* della funzione [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) .</span><span class="sxs-lookup"><span data-stu-id="7fe77-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fe77-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fe77-139">Return value</span></span>

<span data-ttu-id="7fe77-140">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7fe77-140">Type: **UINT**</span></span>

<span data-ttu-id="7fe77-141">Valore diverso da zero se ha esito positivo; in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="7fe77-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fe77-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fe77-142">Remarks</span></span>

<span data-ttu-id="7fe77-143">**SHExtractIconsW** estrae dai tipi di file seguenti.</span><span class="sxs-lookup"><span data-stu-id="7fe77-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="7fe77-144">Eseguibile (con estensione exe)</span><span class="sxs-lookup"><span data-stu-id="7fe77-144">Executable (.exe)</span></span>
-   <span data-ttu-id="7fe77-145">DLL (. dll)</span><span class="sxs-lookup"><span data-stu-id="7fe77-145">DLL (.dll)</span></span>
-   <span data-ttu-id="7fe77-146">Icona (. ico)</span><span class="sxs-lookup"><span data-stu-id="7fe77-146">Icon (.ico)</span></span>
-   <span data-ttu-id="7fe77-147">Cursore (. cur)</span><span class="sxs-lookup"><span data-stu-id="7fe77-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="7fe77-148">Cursore animato (. ani)</span><span class="sxs-lookup"><span data-stu-id="7fe77-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="7fe77-149">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="7fe77-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="7fe77-150">Estrazioni da Windows 3. sono supportati anche file eseguibili *a 16 bit* (con estensione exe o dll).</span><span class="sxs-lookup"><span data-stu-id="7fe77-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="7fe77-151">I parametri *cxIcon* e *cyIcon* specificano le dimensioni delle icone da estrarre.</span><span class="sxs-lookup"><span data-stu-id="7fe77-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="7fe77-152">È possibile estrarre due dimensioni tramite ogni parametro suddividendo il valore tra il relativo LOWORD e HIWORD.</span><span class="sxs-lookup"><span data-stu-id="7fe77-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="7fe77-153">Inserire la prima dimensione desiderata nell'LOWORD del parametro e la seconda dimensione in HIWORD.</span><span class="sxs-lookup"><span data-stu-id="7fe77-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="7fe77-154">Ad esempio, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) per *cxIcon* e *cyIcon* estrae entrambe le icone di dimensioni 24 e 48.</span><span class="sxs-lookup"><span data-stu-id="7fe77-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="7fe77-155">Il processo chiamante è responsabile dell'eliminazione di tutte le icone estratte tramite questa funzione chiamando la funzione [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) .</span><span class="sxs-lookup"><span data-stu-id="7fe77-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="7fe77-156">**SHExtractIconsW** non viene esportato in base al nome o dichiarata in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="7fe77-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="7fe77-157">Per usarlo, è necessario dichiarare un prototipo corrispondente e usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per richiedere un puntatore a funzione da Shell32.dll che può essere usato per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="7fe77-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe77-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fe77-158">Requirements</span></span>



| <span data-ttu-id="7fe77-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fe77-159">Requirement</span></span> | <span data-ttu-id="7fe77-160">Valore</span><span class="sxs-lookup"><span data-stu-id="7fe77-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe77-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe77-161">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe77-162">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fe77-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe77-163">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe77-164">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fe77-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7fe77-165">DLL</span><span class="sxs-lookup"><span data-stu-id="7fe77-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fe77-166"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe77-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="7fe77-167">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7fe77-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7fe77-168">**SHExtractIconsW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="7fe77-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
