---
description: Determina se le impostazioni locali specificate per nome sono installate o supportate nel sistema operativo.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Funzione RtlIsValidLocaleName (Ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879097"
---
# <a name="rtlisvalidlocalename-function"></a><span data-ttu-id="0e3e6-103">RtlIsValidLocaleName (funzione)</span><span class="sxs-lookup"><span data-stu-id="0e3e6-103">RtlIsValidLocaleName function</span></span>

<span data-ttu-id="0e3e6-104">Determina se le impostazioni locali specificate per nome sono installate o supportate nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-104">Determines if a locale specified by name is installed or supported on the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="0e3e6-105">Questa funzione è disponibile per l'utilizzo solo in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-105">This function is available for use in Windows Vista only.</span></span> <span data-ttu-id="0e3e6-106">Potrebbe essere modificato o non disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-106">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0e3e6-107">Le applicazioni devono usare [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="0e3e6-107">Applications should use [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0e3e6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e3e6-108">Syntax</span></span>


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a><span data-ttu-id="0e3e6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e3e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e3e6-110">*LocaleName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e3e6-110">*LocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e3e6-111">[Nome delle impostazioni locali](locale-names.md) da convalidare.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-111">[Locale name](locale-names.md) to validate.</span></span> <span data-ttu-id="0e3e6-112">Questo parametro può specificare il nome di [impostazioni locali personalizzate](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="0e3e6-112">This parameter can specify the name of a [custom locale](custom-locales.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e3e6-113">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e3e6-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e3e6-114">Flag che indicano se le impostazioni locali non associate ad alcun paese sono considerate valide.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-114">Flags indicating if neutral locales are considered valid.</span></span> <span data-ttu-id="0e3e6-115">Attualmente l'unico flag definito è [impostazioni locali \_ Consenti \_ neutro](locale-allow-neutral.md).</span><span class="sxs-lookup"><span data-stu-id="0e3e6-115">Currently the only defined flag is [LOCALE\_ALLOW\_NEUTRAL](locale-allow-neutral.md).</span></span> <span data-ttu-id="0e3e6-116">Il valore predefinito è che non lo sono.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-116">The default value is that they are not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e3e6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e3e6-117">Return value</span></span>

<span data-ttu-id="0e3e6-118">Restituisce un valore diverso da zero se ha esito positivo; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-118">Returns a nonzero value if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e3e6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e3e6-119">Remarks</span></span>

<span data-ttu-id="0e3e6-120">Questa funzione è simile a [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="0e3e6-120">This function is similar to [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span> <span data-ttu-id="0e3e6-121">L'unica differenza è che se le impostazioni locali \_ consentono l' \_ impostazione della lingua neutra, **RtlIsValidLocaleName** restituisce **true** per un nome che corrisponde a impostazioni locali non associate ad alcun paese, ad esempio "en", mentre [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) restituisce **true** solo per le impostazioni locali specifiche, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="0e3e6-121">The only difference is that if LOCALE\_ALLOW\_NEUTRAL is set, **RtlIsValidLocaleName** returns **TRUE** for a name that corresponds to a neutral locale (such as "en"), while [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) returns **TRUE** only for a specific locale (such as "en-US").</span></span> <span data-ttu-id="0e3e6-122">Le impostazioni locali neutre vengono utilizzate come parte della strategia di caricamento delle risorse in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-122">Neutral locales are used as part of the resource loading strategy in Windows Vista and later.</span></span> <span data-ttu-id="0e3e6-123">Solo una piccola classe di applicazioni altamente specializzate utilizza **RtlIsValidLocaleName** e le impostazioni locali \_ consentono la \_ neutralità, perché le impostazioni locali neutre sono di uso molto limitato.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-123">Only a small class of highly specialized applications use **RtlIsValidLocaleName** and set LOCALE\_ALLOW\_NEUTRAL, because neutral locales are of very limited use.</span></span> <span data-ttu-id="0e3e6-124">Nessuna delle funzioni descritte nella [chiamata delle funzioni "nome delle impostazioni locali"](calling-the--locale-name--functions.md) accetta impostazioni locali neutre come input.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-124">None of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e3e6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e3e6-125">Requirements</span></span>



| <span data-ttu-id="0e3e6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e3e6-126">Requirement</span></span> | <span data-ttu-id="0e3e6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0e3e6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3e6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e3e6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0e3e6-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e3e6-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e3e6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e3e6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0e3e6-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e3e6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e3e6-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e3e6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e3e6-133"><dt>Ntrtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e3e6-133"><dt>Ntrtl.h</dt></span></span> </dl>      |
| <span data-ttu-id="0e3e6-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e3e6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e3e6-135"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e3e6-135"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e3e6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0e3e6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e3e6-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e3e6-137"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e3e6-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e3e6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e3e6-139">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="0e3e6-139">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="0e3e6-140">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="0e3e6-140">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="0e3e6-141">**IsValidLocaleName**</span><span class="sxs-lookup"><span data-stu-id="0e3e6-141">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




