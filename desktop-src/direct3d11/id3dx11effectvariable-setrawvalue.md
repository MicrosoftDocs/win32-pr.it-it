---
title: Metodo ID3DX11EffectVariable SetRawValue (D3dx11effect. h)
description: Impostare i dati.
ms.assetid: c5d53aa6-6cd8-4a93-9851-2a93bc6a728a
keywords:
- Metodo SetRawValue Direct3D 11
- Metodo SetRawValue Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo SetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.SetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5186e55b8b1d3472cb25ea6fa067988d4fb1f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234948"
---
# <a name="id3dx11effectvariablesetrawvalue-method"></a><span data-ttu-id="f3759-106">Metodo ID3DX11EffectVariable:: SetRawValue</span><span class="sxs-lookup"><span data-stu-id="f3759-106">ID3DX11EffectVariable::SetRawValue method</span></span>

<span data-ttu-id="f3759-107">Impostare i dati.</span><span class="sxs-lookup"><span data-stu-id="f3759-107">Set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3759-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3759-108">Syntax</span></span>


```C++
HRESULT SetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="f3759-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3759-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3759-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="f3759-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f3759-111">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="f3759-111">Type: **void\***</span></span>

<span data-ttu-id="f3759-112">Puntatore alla variabile.</span><span class="sxs-lookup"><span data-stu-id="f3759-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="f3759-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="f3759-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="f3759-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3759-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f3759-115">Offset (in byte) dall'inizio del puntatore ai dati.</span><span class="sxs-lookup"><span data-stu-id="f3759-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="f3759-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="f3759-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="f3759-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f3759-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f3759-118">Numero di byte da impostare.</span><span class="sxs-lookup"><span data-stu-id="f3759-118">The number of bytes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3759-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3759-119">Return value</span></span>

<span data-ttu-id="f3759-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3759-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3759-121">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f3759-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3759-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3759-122">Remarks</span></span>

<span data-ttu-id="f3759-123">Questo metodo non esegue alcuna conversione o controllo dei tipi; si tratta quindi di un modo molto rapido per accedere agli elementi della matrice.</span><span class="sxs-lookup"><span data-stu-id="f3759-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="f3759-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f3759-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f3759-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f3759-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f3759-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f3759-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3759-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3759-127">Requirements</span></span>



| <span data-ttu-id="f3759-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3759-128">Requirement</span></span> | <span data-ttu-id="f3759-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f3759-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3759-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3759-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f3759-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3759-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f3759-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="f3759-132">Library</span></span><br/> | <dl> <span data-ttu-id="f3759-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f3759-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3759-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3759-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3759-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="f3759-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

