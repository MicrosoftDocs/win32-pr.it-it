---
title: attributo Code
description: L'attributo \ code \ ACF causa la generazione del codice stub client per le funzioni remote.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- attributo Code MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334668"
---
# <a name="code-attribute"></a><span data-ttu-id="7bfcf-104">attributo Code</span><span class="sxs-lookup"><span data-stu-id="7bfcf-104">code attribute</span></span>

<span data-ttu-id="7bfcf-105">L'attributo **\[ Code \]** ACF causa la generazione di codice stub client per le funzioni remote.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-105">The **\[code\]** ACF attribute causes client stub code to be generated for remote functions.</span></span>

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="7bfcf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bfcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bfcf-107">*Attributi di interfaccia ACF*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-108">Specifica un elenco di uno o più attributi che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="7bfcf-109">Gli attributi validi includono [**\[ \_ handle \] automatico**](auto-handle.md) o [**\[ \_ handle \] implicito**](implicit-handle.md) , ovvero **\[ codice \]**, [**\[ NoCode \]**](nocode.md)o [**\[ optimize \]**](optimize.md).</span><span class="sxs-lookup"><span data-stu-id="7bfcf-109">Valid attributes include either [**\[auto\_handle\]**](auto-handle.md) or [**\[implicit\_handle\]**](implicit-handle.md) and either **\[code\]**, [**\[nocode\]**](nocode.md), or [**\[optimize\]**](optimize.md).</span></span> <span data-ttu-id="7bfcf-110">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="7bfcf-111">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-112">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-112">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7bfcf-113">*elenco filename*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-113">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-114">Specifica un elenco di uno o più nomi di file di intestazione C separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-114">Specifies a list of one or more C-header file names, separated by commas.</span></span> <span data-ttu-id="7bfcf-115">È necessario specificare il nome completo del file, inclusa l'estensione.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-115">You must supply the full file name, including the extension.</span></span>

</dd> <dt>

<span data-ttu-id="7bfcf-116">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-116">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-117">Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-117">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="7bfcf-118">Gli attributi di tipo validi includono [**\[ \] allocate**](allocate.md) e [**\[ rappresentano \_ come \]**](represent-as.md).</span><span class="sxs-lookup"><span data-stu-id="7bfcf-118">Valid type attributes include [**\[allocate\]**](allocate.md) and [**\[represent\_as\]**](represent-as.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bfcf-119">*typeName*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-119">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-120">Specifica un tipo definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-120">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="7bfcf-121">Gli attributi di tipo in ACF possono essere applicati solo ai tipi definiti in precedenza nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-121">Type attributes in the ACF can be applied only to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="7bfcf-122">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-122">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-123">Specifica zero o più attributi che si applicano alla funzione nel suo complesso, ad esempio [**\[ \_ lo \] stato della comunicazione**](comm-status.md).</span><span class="sxs-lookup"><span data-stu-id="7bfcf-123">Specifies zero or more attributes that apply to the function as a whole, such as [**\[comm\_status\]**](comm-status.md).</span></span> <span data-ttu-id="7bfcf-124">Gli attributi della funzione sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-124">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="7bfcf-125">Separare più attributi di funzione con virgole.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-125">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="7bfcf-126">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-126">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-127">Specifica il nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-127">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="7bfcf-128">*ACF-parametri-attributi*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-128">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-129">Specifica gli attributi ACF che si applicano a un parametro.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-129">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="7bfcf-130">Si noti che è possibile applicare zero, uno o più attributi al parametro.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-130">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="7bfcf-131">Separare più attributi di parametro con virgole.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-131">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="7bfcf-132">Gli attributi del parametro ACF sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-132">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="7bfcf-133">*Nome parametro*</span><span class="sxs-lookup"><span data-stu-id="7bfcf-133">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfcf-134">Specifica un parametro della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-134">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="7bfcf-135">Ogni parametro per la funzione deve essere specificato nella stessa sequenza e con lo stesso nome definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-135">Each parameter for the function must be specified in the same sequence and with the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bfcf-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bfcf-136">Remarks</span></span>

<span data-ttu-id="7bfcf-137">L'attributo **\[ Code \]** può essere visualizzato nell'intestazione ACF o essere applicato a una singola funzione.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-137">The **\[code\]** attribute can appear in the ACF header or be applied to an individual function.</span></span>

<span data-ttu-id="7bfcf-138">Quando l'attributo **\[ Code \]** viene visualizzato nell'intestazione ACF, viene generato il codice stub client per tutte le funzioni remote che non dispongono dell'attributo della funzione [**\[ NoCode \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="7bfcf-138">When the **\[code\]** attribute appears in the ACF header, client stub code is generated for all remote functions that do not have the [**\[nocode\]**](nocode.md) function attribute.</span></span> <span data-ttu-id="7bfcf-139">È possibile eseguire l'override dell'attributo **\[ Code \]** nell'intestazione per una singola funzione specificando l'attributo **\[ NoCode \]** come attributo della funzione.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-139">You can override the **\[code\]** attribute in the header for an individual function by specifying the **\[nocode\]** attribute as a function attribute.</span></span>

<span data-ttu-id="7bfcf-140">Quando l'attributo **\[ Code \]** viene visualizzato nell'elenco di attributi della funzione remota, viene generato il codice stub client per la funzione.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-140">When the **\[code\]** attribute appears in the remote function's attribute list, client stub code is generated for the function.</span></span> <span data-ttu-id="7bfcf-141">Il codice stub client non viene generato quando:</span><span class="sxs-lookup"><span data-stu-id="7bfcf-141">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="7bfcf-142">L'intestazione ACF include l'attributo [**\[ NoCode \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="7bfcf-142">The ACF header includes the [**\[nocode\]**](nocode.md) attribute.</span></span>
-   <span data-ttu-id="7bfcf-143">L'attributo [**\[ NoCode \]**](nocode.md) viene applicato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-143">The [**\[nocode\]**](nocode.md) attribute is applied to the function.</span></span>
-   <span data-ttu-id="7bfcf-144">L'attributo [**\[ Local \]**](local.md) si applica alla funzione nel file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-144">The [**\[local\]**](local.md) attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="7bfcf-145">Il **\[ codice \]** o [**\[ NoCode \]**](nocode.md) può essere visualizzato nell'elenco di attributi dell'interfaccia o della funzione, ma quello scelto può comparire una sola volta nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7bfcf-145">Either **\[code\]** or [**\[nocode\]**](nocode.md) can appear in the interface or function attribute list, but the one you choose can appear only once in the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bfcf-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bfcf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bfcf-147">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="7bfcf-147">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="7bfcf-148">**allocare**</span><span class="sxs-lookup"><span data-stu-id="7bfcf-148">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="7bfcf-149">**\_handle automatico**</span><span class="sxs-lookup"><span data-stu-id="7bfcf-149">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="7bfcf-150">**stato di comunicazione \_**</span><span class="sxs-lookup"><span data-stu-id="7bfcf-150">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="7bfcf-151">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="7bfcf-151">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="7bfcf-152">**locale**</span><span class="sxs-lookup"><span data-stu-id="7bfcf-152">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="7bfcf-153">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="7bfcf-153">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="7bfcf-154">**ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="7bfcf-154">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="7bfcf-155">**rappresenta \_ come**</span><span class="sxs-lookup"><span data-stu-id="7bfcf-155">**represent\_as**</span></span>](represent-as.md)
</dt> </dl>

 

 




