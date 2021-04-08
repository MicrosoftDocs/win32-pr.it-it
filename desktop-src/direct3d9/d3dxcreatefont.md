---
description: Crea un oggetto del tipo di carattere per un dispositivo e un tipo di carattere.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Funzione D3DXCreateFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762191"
---
# <a name="d3dxcreatefont-function"></a><span data-ttu-id="eb1a3-103">D3DXCreateFont (funzione)</span><span class="sxs-lookup"><span data-stu-id="eb1a3-103">D3DXCreateFont function</span></span>

<span data-ttu-id="eb1a3-104">Crea un oggetto del tipo di carattere per un dispositivo e un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-104">Creates a font object for a device and font.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1a3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb1a3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="eb1a3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb1a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb1a3-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="eb1a3-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , il dispositivo da associare all'oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-110">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-111">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-111">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-112">Altezza dei caratteri nelle unità logiche.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-112">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-113">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-113">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-115">Larghezza dei caratteri nelle unità logiche.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-115">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-116">*Peso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-116">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-118">Spessore carattere.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-118">Typeface weight.</span></span> <span data-ttu-id="eb1a3-119">Un esempio è grassetto.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-119">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-120">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-122">Il numero di livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-122">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-123">*Corsivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-123">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-124">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-124">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-125">True per il tipo di carattere corsivo, false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-125">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-126">*Set di caratteri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-126">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-128">Set di caratteri del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-128">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-129">*OutputPrecision* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-129">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-131">Specifica il modo in cui Windows deve tentare di trovare le dimensioni e le caratteristiche dei caratteri desiderate con i tipi di carattere effettivi</span><span class="sxs-lookup"><span data-stu-id="eb1a3-131">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="eb1a3-132">Usare OUT \_ TT \_ solo \_ per l'istanza, per assicurarsi di ottenere sempre un tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-132">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-133">*Qualità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-133">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-135">Specifica il modo in cui Windows deve corrispondere al tipo di carattere desiderato con un tipo di carattere reale.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-135">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="eb1a3-136">Si applica solo ai tipi di carattere raster e non deve influire sui tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-136">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-137">*PitchAndFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-137">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-139">Indice di passo e famiglia.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-139">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-140">*pFacename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-140">*pFacename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-141">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-141">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb1a3-142">Stringa contenente il nome del carattere tipografico.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-142">String containing the typeface name.</span></span> <span data-ttu-id="eb1a3-143">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-143">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="eb1a3-144">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-144">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="eb1a3-145">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-145">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="eb1a3-146">*ppFont* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eb1a3-146">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb1a3-147">Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb1a3-147">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="eb1a3-148">Restituisce un puntatore a un'interfaccia [**ID3DXFont**](id3dxfont.md) , che rappresenta l'oggetto del tipo di carattere creato.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-148">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb1a3-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb1a3-149">Return value</span></span>

<span data-ttu-id="eb1a3-150">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb1a3-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb1a3-151">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-151">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="eb1a3-152">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-152">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb1a3-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb1a3-153">Remarks</span></span>

<span data-ttu-id="eb1a3-154">Per la creazione di un oggetto ID3DXFont è necessario che il dispositivo supporti il colore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-154">The creation of an ID3DXFont object requires that the device supports 32-bit color.</span></span>

<span data-ttu-id="eb1a3-155">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="eb1a3-156">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="eb1a3-157">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateFontA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="eb1a3-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="eb1a3-158">Per ulteriori informazioni sui parametri dei tipi di carattere, vedere [il tipo di carattere logico](../gdi/creating-a-logical-font.md).</span><span class="sxs-lookup"><span data-stu-id="eb1a3-158">If you want more information about font parameters, see [The Logical Font](../gdi/creating-a-logical-font.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb1a3-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb1a3-159">Requirements</span></span>



| <span data-ttu-id="eb1a3-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb1a3-160">Requirement</span></span> | <span data-ttu-id="eb1a3-161">Valore</span><span class="sxs-lookup"><span data-stu-id="eb1a3-161">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1a3-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb1a3-162">Header</span></span><br/>  | <dl> <span data-ttu-id="eb1a3-163"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb1a3-163"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="eb1a3-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb1a3-164">Library</span></span><br/> | <dl> <span data-ttu-id="eb1a3-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb1a3-165"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb1a3-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb1a3-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1a3-167">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="eb1a3-167">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
