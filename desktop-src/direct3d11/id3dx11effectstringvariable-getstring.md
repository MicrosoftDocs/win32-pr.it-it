---
title: Metodo GetString ID3DX11EffectStringVariable (D3dx11effect. h)
description: Ottiene la stringa.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- Metodo GetString Direct3D 11
- Metodo GetString Direct3D 11, interfaccia ID3DX11EffectStringVariable
- Interfaccia ID3DX11EffectStringVariable Direct3D 11, metodo GetString
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982142"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a><span data-ttu-id="7bf84-106">Metodo ID3DX11EffectStringVariable:: GetString</span><span class="sxs-lookup"><span data-stu-id="7bf84-106">ID3DX11EffectStringVariable::GetString method</span></span>

<span data-ttu-id="7bf84-107">Ottiene la stringa.</span><span class="sxs-lookup"><span data-stu-id="7bf84-107">Get the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf84-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bf84-108">Syntax</span></span>


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="7bf84-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bf84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bf84-110">*ppString*</span><span class="sxs-lookup"><span data-stu-id="7bf84-110">*ppString*</span></span> 
</dt> <dd>

<span data-ttu-id="7bf84-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="7bf84-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="7bf84-112">Puntatore alla stringa.</span><span class="sxs-lookup"><span data-stu-id="7bf84-112">A pointer to the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bf84-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bf84-113">Return value</span></span>

<span data-ttu-id="7bf84-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7bf84-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7bf84-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7bf84-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf84-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bf84-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7bf84-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="7bf84-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7bf84-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7bf84-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7bf84-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7bf84-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7bf84-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bf84-120">Requirements</span></span>



| <span data-ttu-id="7bf84-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bf84-121">Requirement</span></span> | <span data-ttu-id="7bf84-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf84-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf84-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bf84-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7bf84-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf84-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7bf84-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="7bf84-125">Library</span></span><br/> | <dl> <span data-ttu-id="7bf84-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="7bf84-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf84-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bf84-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf84-128">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="7bf84-128">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

