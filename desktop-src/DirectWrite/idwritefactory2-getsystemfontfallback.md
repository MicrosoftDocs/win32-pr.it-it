---
title: Metodo IDWriteFactory2 GetSystemFontFallback
description: Crea un oggetto fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Scrittura diretta metodo GetSystemFontFallback
- Metodo GetSystemFontFallback scrittura diretta, interfaccia IDWriteFactory2
- IDWriteFactory2 Interface Direct Write, metodo GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399472"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a><span data-ttu-id="9e572-106">Metodo IDWriteFactory2:: GetSystemFontFallback</span><span class="sxs-lookup"><span data-stu-id="9e572-106">IDWriteFactory2::GetSystemFontFallback method</span></span>

<span data-ttu-id="9e572-107">Crea un oggetto fallback del tipo di carattere dall'elenco di fallback dei tipi di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="9e572-107">Creates a font fallback object from the system font fallback list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e572-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e572-108">Syntax</span></span>


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a><span data-ttu-id="9e572-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e572-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e572-110">*fontFallback* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e572-110">*fontFallback* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e572-111">Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span><span class="sxs-lookup"><span data-stu-id="9e572-111">Type: **[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span></span>

<span data-ttu-id="9e572-112">Contiene un indirizzo di un puntatore all'oggetto fallback del tipo di carattere appena creato.</span><span class="sxs-lookup"><span data-stu-id="9e572-112">Contains an address of a pointer to the newly created font fallback object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e572-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e572-113">Return value</span></span>

<span data-ttu-id="9e572-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9e572-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9e572-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9e572-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e572-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e572-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e572-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e572-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e572-118">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="9e572-118">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

 