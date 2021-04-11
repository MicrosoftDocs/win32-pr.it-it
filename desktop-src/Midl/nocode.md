---
title: NoCode (attributo)
description: L'attributo \ NoCode \ viene usato nelle intestazioni ACF o con singole funzioni per impedire la generazione di codice stub del client.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- NoCode (attributo MIDL)
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333575"
---
# <a name="nocode-attribute"></a><span data-ttu-id="247b9-104">NoCode (attributo)</span><span class="sxs-lookup"><span data-stu-id="247b9-104">nocode attribute</span></span>

<span data-ttu-id="247b9-105">L'attributo **\[ NoCode \]** viene usato nelle intestazioni ACF o con singole funzioni per impedire la generazione di codice stub del client.</span><span class="sxs-lookup"><span data-stu-id="247b9-105">The **\[nocode\]** attribute is used in ACF headers or with individual functions to prevent the generation of client stub code.</span></span>

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="247b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="247b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="247b9-107">*Attributi di interfaccia ACF*</span><span class="sxs-lookup"><span data-stu-id="247b9-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-108">Specifica un elenco di uno o più attributi che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="247b9-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="247b9-109">Gli attributi validi includono **\[** [**\_ handle automatico**](auto-handle.md) **\]** o **\[** [**\_ handle implicito**](implicit-handle.md) **\]** e **\[** [**codice**](code.md) **\]** o **\[ NoCode \]**.</span><span class="sxs-lookup"><span data-stu-id="247b9-109">Valid attributes include either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]** and either **\[**[**code**](code.md)**\]** or **\[nocode\]**.</span></span> <span data-ttu-id="247b9-110">Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="247b9-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="247b9-111">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="247b9-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-112">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="247b9-112">Specifies the name of the interface.</span></span> <span data-ttu-id="247b9-113">In modalità di compatibilità DCE, il nome dell'interfaccia deve corrispondere al nome dell'interfaccia specificata nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="247b9-113">In DCE-compatibility mode, the interface name must match the name of the interface specified in the IDL file.</span></span> <span data-ttu-id="247b9-114">Quando si usa l'opzione del compilatore MIDL [**/ACF**](-acf.md), il nome dell'interfaccia in ACF e il nome dell'interfaccia nel file IDL possono essere diversi.</span><span class="sxs-lookup"><span data-stu-id="247b9-114">When you use the MIDL compiler switch [**/acf**](-acf.md), the interface name in the ACF and the interface name in the IDL file can be different.</span></span>

</dd> <dt>

<span data-ttu-id="247b9-115">*elenco filename*</span><span class="sxs-lookup"><span data-stu-id="247b9-115">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-116">Specifica un elenco di uno o più nomi di file di intestazione del linguaggio C, separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="247b9-116">Specifies a list of one or more C-language header file names, separated by commas.</span></span> <span data-ttu-id="247b9-117">È necessario specificare il nome completo del file, inclusa l'estensione.</span><span class="sxs-lookup"><span data-stu-id="247b9-117">The full file name, including the extension, must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="247b9-118">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="247b9-118">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-119">Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="247b9-119">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="247b9-120">Gli attributi di tipo validi includono **\[** [**allocate**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="247b9-120">Valid type attributes include **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="247b9-121">*typeName*</span><span class="sxs-lookup"><span data-stu-id="247b9-121">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-122">Specifica un tipo definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="247b9-122">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="247b9-123">Gli attributi di tipo in ACF possono essere applicati solo ai tipi definiti in precedenza nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="247b9-123">Type attributes in the ACF can only be applied to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="247b9-124">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="247b9-124">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-125">Specifica gli attributi che si applicano alla funzione nel suo complesso, ad esempio **\[** [**\_ lo stato della comunicazione**](comm-status.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="247b9-125">Specifies attributes that apply to the function as a whole, such as **\[**[**comm\_status**](comm-status.md)**\]**.</span></span> <span data-ttu-id="247b9-126">Gli attributi della funzione sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="247b9-126">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="247b9-127">Separare più attributi di funzione con virgole.</span><span class="sxs-lookup"><span data-stu-id="247b9-127">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="247b9-128">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="247b9-128">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-129">Specifica il nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="247b9-129">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="247b9-130">*ACF-parametri-attributi*</span><span class="sxs-lookup"><span data-stu-id="247b9-130">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-131">Specifica gli attributi ACF che si applicano a un parametro.</span><span class="sxs-lookup"><span data-stu-id="247b9-131">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="247b9-132">Si noti che è possibile applicare zero o più attributi al parametro.</span><span class="sxs-lookup"><span data-stu-id="247b9-132">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="247b9-133">Separare più attributi di parametro con virgole.</span><span class="sxs-lookup"><span data-stu-id="247b9-133">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="247b9-134">Gli attributi del parametro ACF sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="247b9-134">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="247b9-135">*Nome parametro*</span><span class="sxs-lookup"><span data-stu-id="247b9-135">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="247b9-136">Specifica un parametro della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="247b9-136">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="247b9-137">Ogni parametro per la funzione deve essere specificato nella stessa sequenza e utilizzando lo stesso nome definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="247b9-137">Each parameter for the function must be specified in the same sequence and using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="247b9-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="247b9-138">Remarks</span></span>

<span data-ttu-id="247b9-139">L'attributo **\[ NoCode \]** può essere visualizzato nell'intestazione ACF oppure può essere applicato a una singola funzione.</span><span class="sxs-lookup"><span data-stu-id="247b9-139">The **\[nocode\]** attribute can appear in the ACF header, or it can be applied to an individual function.</span></span>

<span data-ttu-id="247b9-140">Quando l'attributo **\[ \] NoCode** viene visualizzato nell'intestazione ACF, il codice stub del client non viene generato per alcuna funzione remota a meno che non disponga dell'attributo della funzione di **\[** [**codice**](code.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="247b9-140">When the **\[nocode\]** attribute appears in the ACF header, client stub code is not generated for any remote function unless it has the **\[**[**code**](code.md)**\]** function attribute.</span></span> <span data-ttu-id="247b9-141">È possibile eseguire l'override dell'attributo **\[ NoCode \]** nell'intestazione per una singola funzione specificando l'attributo **\[ Code \]** come attributo della funzione.</span><span class="sxs-lookup"><span data-stu-id="247b9-141">You can override the **\[nocode\]** attribute in the header for an individual function by specifying the **\[code\]** attribute as a function attribute.</span></span>

<span data-ttu-id="247b9-142">Quando l'attributo **\[ NoCode \]** viene visualizzato nell'elenco di attributi della funzione, per la funzione non viene generato alcun codice stub client.</span><span class="sxs-lookup"><span data-stu-id="247b9-142">When the **\[nocode\]** attribute appears in the function's attribute list, no client stub code is generated for the function.</span></span>

<span data-ttu-id="247b9-143">Il codice stub client non viene generato quando:</span><span class="sxs-lookup"><span data-stu-id="247b9-143">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="247b9-144">L'intestazione ACF include l'attributo **\[ NoCode \]** .</span><span class="sxs-lookup"><span data-stu-id="247b9-144">The ACF header includes the **\[nocode\]** attribute.</span></span>
-   <span data-ttu-id="247b9-145">L'attributo **\[ NoCode \]** viene applicato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="247b9-145">The **\[nocode\]** attribute is applied to the function.</span></span>
-   <span data-ttu-id="247b9-146">L' **\[** attributo [**local**](local.md) **\]** si applica alla funzione nel file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="247b9-146">The **\[**[**local**](local.md)**\]** attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="247b9-147">Il **\[** [**codice**](code.md) **\]** o **\[ NoCode \]** può essere visualizzato nell'elenco di attributi di una funzione e quello scelto può essere visualizzato esattamente una volta.</span><span class="sxs-lookup"><span data-stu-id="247b9-147">Either **\[**[**code**](code.md)**\]** or **\[nocode\]** can appear in a function's attribute list, and the one you choose can appear exactly once.</span></span>

<span data-ttu-id="247b9-148">L'attributo **\[ NoCode \]** viene ignorato quando vengono generati stub server.</span><span class="sxs-lookup"><span data-stu-id="247b9-148">The **\[nocode\]** attribute is ignored when server stubs are generated.</span></span> <span data-ttu-id="247b9-149">Non è possibile applicarlo quando si generano stub server in modalità di compatibilità DCE.</span><span class="sxs-lookup"><span data-stu-id="247b9-149">You cannot apply it when generating server stubs in DCE-compatibility mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="247b9-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="247b9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="247b9-151">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="247b9-151">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="247b9-152">**/acf**</span><span class="sxs-lookup"><span data-stu-id="247b9-152">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="247b9-153">**allocare**</span><span class="sxs-lookup"><span data-stu-id="247b9-153">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="247b9-154">**\_handle automatico**</span><span class="sxs-lookup"><span data-stu-id="247b9-154">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="247b9-155">**codice**</span><span class="sxs-lookup"><span data-stu-id="247b9-155">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="247b9-156">**stato di comunicazione \_**</span><span class="sxs-lookup"><span data-stu-id="247b9-156">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="247b9-157">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="247b9-157">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> </dl>

 

 




