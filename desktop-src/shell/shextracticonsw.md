---
description: Crea una matrice di handle per le icone estratte da un file specificato.
title: Funzione SHExtractIconsW
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
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840912"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="81d08-103">Funzione SHExtractIconsW</span><span class="sxs-lookup"><span data-stu-id="81d08-103">SHExtractIconsW function</span></span>

<span data-ttu-id="81d08-104">\[**SHExtractIconsW** è disponibile tramite Windows XP Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="81d08-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="81d08-105">Potrebbe essere modificato o non disponibile nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="81d08-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="81d08-106">Crea una matrice di handle per le icone estratte da un file specificato.</span><span class="sxs-lookup"><span data-stu-id="81d08-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d08-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81d08-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="81d08-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81d08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81d08-109">*pszFileName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="81d08-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d08-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="81d08-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="81d08-111">Puntatore al nome del file da cui estrarre le icone.</span><span class="sxs-lookup"><span data-stu-id="81d08-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="81d08-112">*nIconIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="81d08-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d08-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="81d08-113">Type: **int**</span></span>

<span data-ttu-id="81d08-114">Indice della prima icona da estrarre dalla risorsa denominata in *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="81d08-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="81d08-115">*cxIcon* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="81d08-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d08-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="81d08-116">Type: **int**</span></span>

<span data-ttu-id="81d08-117">Larghezza desiderata dell'icona.</span><span class="sxs-lookup"><span data-stu-id="81d08-117">The desired width of the icon.</span></span> <span data-ttu-id="81d08-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="81d08-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="81d08-119">*cyIcon* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="81d08-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d08-120">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="81d08-120">Type: **int**</span></span>

<span data-ttu-id="81d08-121">Altezza desiderata dell'icona.</span><span class="sxs-lookup"><span data-stu-id="81d08-121">The desired height of the icon.</span></span> <span data-ttu-id="81d08-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="81d08-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="81d08-123">*phIcon* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="81d08-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81d08-124">Tipo: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="81d08-124">Type: **HICON\***</span></span>

<span data-ttu-id="81d08-125">Quando questa funzione viene restituita, contiene un puntatore alla matrice di handle di icona.</span><span class="sxs-lookup"><span data-stu-id="81d08-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="81d08-126">*pIconId* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="81d08-126">*pIconId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81d08-127">Tipo: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="81d08-127">Type: **UINT\***</span></span>

<span data-ttu-id="81d08-128">Quando questa funzione viene restituita, contiene un puntatore all'identificatore di risorsa dell'icona estratta più adatta al dispositivo di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="81d08-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="81d08-129">Se non è disponibile alcun identificatore per questo formato, contiene 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="81d08-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="81d08-130">Se non è possibile ottenere alcun identificatore per qualsiasi altro motivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="81d08-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="81d08-131">*nIcons* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="81d08-131">*nIcons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d08-132">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="81d08-132">Type: **UINT**</span></span>

<span data-ttu-id="81d08-133">Numero di icone da estrarre dalla risorsa denominata in *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="81d08-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="81d08-134">Questo parametro è valido solo quando la risorsa è un file con estensione exe o dll.</span><span class="sxs-lookup"><span data-stu-id="81d08-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="81d08-135">*flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="81d08-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d08-136">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="81d08-136">Type: **UINT**</span></span>

<span data-ttu-id="81d08-137">Flag che controllano questa funzione.</span><span class="sxs-lookup"><span data-stu-id="81d08-137">The flags that control this function.</span></span> <span data-ttu-id="81d08-138">Per i valori possibili, vedere il *parametro fuLoad* della [**funzione LoadImage.**](/windows/win32/api/winuser/nf-winuser-loadimagea)</span><span class="sxs-lookup"><span data-stu-id="81d08-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81d08-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81d08-139">Return value</span></span>

<span data-ttu-id="81d08-140">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="81d08-140">Type: **UINT**</span></span>

<span data-ttu-id="81d08-141">Valore diverso da zero in caso di esito positivo. in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="81d08-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="81d08-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="81d08-142">Remarks</span></span>

<span data-ttu-id="81d08-143">**SHExtractIconsW** estrae dai tipi di file seguenti.</span><span class="sxs-lookup"><span data-stu-id="81d08-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="81d08-144">Eseguibile (con estensione exe)</span><span class="sxs-lookup"><span data-stu-id="81d08-144">Executable (.exe)</span></span>
-   <span data-ttu-id="81d08-145">DLL (.dll)</span><span class="sxs-lookup"><span data-stu-id="81d08-145">DLL (.dll)</span></span>
-   <span data-ttu-id="81d08-146">Icona (.ico)</span><span class="sxs-lookup"><span data-stu-id="81d08-146">Icon (.ico)</span></span>
-   <span data-ttu-id="81d08-147">Cursore (.cur)</span><span class="sxs-lookup"><span data-stu-id="81d08-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="81d08-148">Cursore animato (.ani)</span><span class="sxs-lookup"><span data-stu-id="81d08-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="81d08-149">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="81d08-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="81d08-150">Estrazioni da Windows 3. *Sono* supportati anche i file eseguibili a 16 bit (exe o dll).</span><span class="sxs-lookup"><span data-stu-id="81d08-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="81d08-151">I *parametri cxIcon* *e cyIcon* specificano le dimensioni delle icone da estrarre.</span><span class="sxs-lookup"><span data-stu-id="81d08-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="81d08-152">È possibile estrarre due dimensioni tramite ogni parametro suddividendo il valore tra LOWORD e HIWORD.</span><span class="sxs-lookup"><span data-stu-id="81d08-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="81d08-153">Inserire la prima dimensione desiderata nel valore LOWORD del parametro e la seconda dimensione in HIWORD.</span><span class="sxs-lookup"><span data-stu-id="81d08-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="81d08-154">MakeLONG [](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) per *cxIcon* e *cyIcon,* ad esempio, estrae icone con dimensioni di 24 e 48.</span><span class="sxs-lookup"><span data-stu-id="81d08-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="81d08-155">Il processo chiamante è responsabile dell'eliminazione di tutte le icone estratte tramite questa funzione chiamando la [**funzione DestroyIcon.**](/windows/win32/api/winuser/nf-winuser-destroyicon)</span><span class="sxs-lookup"><span data-stu-id="81d08-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="81d08-156">**SHExtractIconsW** non viene esportato per nome o dichiarato in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="81d08-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="81d08-157">Per usarlo, è necessario dichiarare un prototipo corrispondente e usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per richiedere un puntatore a funzione da Shell32.dll che può essere usato per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="81d08-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="81d08-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81d08-158">Requirements</span></span>



| <span data-ttu-id="81d08-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="81d08-159">Requirement</span></span> | <span data-ttu-id="81d08-160">Valore</span><span class="sxs-lookup"><span data-stu-id="81d08-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81d08-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81d08-161">Minimum supported client</span></span><br/> | <span data-ttu-id="81d08-162">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="81d08-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81d08-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81d08-163">Minimum supported server</span></span><br/> | <span data-ttu-id="81d08-164">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="81d08-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="81d08-165">DLL</span><span class="sxs-lookup"><span data-stu-id="81d08-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81d08-166"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="81d08-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="81d08-167">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="81d08-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="81d08-168">**SHExtractIconsW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="81d08-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
