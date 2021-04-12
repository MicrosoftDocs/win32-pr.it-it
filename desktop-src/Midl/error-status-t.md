---
title: attributo error_status_t
description: La \_ \_ parola chiave Error Status t designa un tipo per un oggetto che contiene informazioni sullo stato di comunicazione o sugli errori.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- attributo error_status_t MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333583"
---
# <a name="error_status_t-attribute"></a><span data-ttu-id="f1026-104">\_attributo stato errore \_ t</span><span class="sxs-lookup"><span data-stu-id="f1026-104">error\_status\_t attribute</span></span>

<span data-ttu-id="f1026-105">La parola chiave **Error \_ status \_ t** designa un tipo per un oggetto che contiene informazioni sullo stato di comunicazione o sugli errori.</span><span class="sxs-lookup"><span data-stu-id="f1026-105">The **error\_status\_t** keyword designates a type for an object that contains communication-status or fault-status information.</span></span>

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="f1026-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1026-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1026-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="f1026-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f1026-108">Specifica zero o più attributi della funzione ACF, ad esempio **\[** [**\_ stato di comunicazione**](comm-status.md) **\]** , **\[** [**\_ stato di errore**](fault-status.md) **\]** o **\[** [**NoCode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f1026-108">Specifies zero or more ACF function attributes, such as **\[**[**comm\_status**](comm-status.md)**\]**, **\[**[**fault\_status**](fault-status.md)**\]**, or **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="f1026-109">Gli attributi della funzione sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="f1026-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="f1026-110">È possibile applicare zero o più attributi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="f1026-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="f1026-111">Separare più attributi di funzione con virgole.</span><span class="sxs-lookup"><span data-stu-id="f1026-111">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="f1026-112">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="f1026-112">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f1026-113">Specifica il nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="f1026-113">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="f1026-114">*ACF-parametri-attributi*</span><span class="sxs-lookup"><span data-stu-id="f1026-114">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f1026-115">Specifica gli attributi che si applicano a un parametro.</span><span class="sxs-lookup"><span data-stu-id="f1026-115">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="f1026-116">Si noti che è possibile applicare zero, uno o più attributi al parametro.</span><span class="sxs-lookup"><span data-stu-id="f1026-116">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="f1026-117">Separare più attributi di parametro con virgole.</span><span class="sxs-lookup"><span data-stu-id="f1026-117">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="f1026-118">Gli attributi di parametro sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="f1026-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="f1026-119">Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF.</span><span class="sxs-lookup"><span data-stu-id="f1026-119">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span>

</dd> <dt>

<span data-ttu-id="f1026-120">*Nome parametro*</span><span class="sxs-lookup"><span data-stu-id="f1026-120">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f1026-121">Specifica il parametro per la funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="f1026-121">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="f1026-122">Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="f1026-122">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1026-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1026-123">Remarks</span></span>

<span data-ttu-id="f1026-124">Il tipo di **stato di errore \_ \_ t** viene usato come parte dell'architettura di gestione delle eccezioni in IDL.</span><span class="sxs-lookup"><span data-stu-id="f1026-124">The **error\_status\_t** type is used as a part of the exception handling architecture in IDL.</span></span> <span data-ttu-id="f1026-125">Questo tipo esegue il mapping a un oggetto [**Long**](long.md) [**senza segno**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="f1026-125">This type maps to an [**unsigned**](unsigned.md) [**long**](long.md).</span></span> <span data-ttu-id="f1026-126">Le applicazioni che intercettano situazioni di errore presentano un **\[** parametro [**out**](out-idl.md) **\]** o un tipo restituito di una procedura specificata come **stato di errore \_ \_ t** e qualificano lo **stato di errore \_ \_ t** con gli attributi di stato **\[** di [**comunicazione \_**](comm-status.md) o di **\]** **\[** [**\_ stato**](fault-status.md) di errore **\]** in ACF.</span><span class="sxs-lookup"><span data-stu-id="f1026-126">Applications that catch error situations have an **\[**[**out**](out-idl.md)**\]** parameter or a return type of a procedure specified as **error\_status\_t**, and qualify the **error\_status\_t** with the **\[**[**comm\_status**](comm-status.md)**\]** or **\[**[**fault\_status**](fault-status.md)**\]** attributes in the ACF.</span></span> <span data-ttu-id="f1026-127">Se il parametro o il tipo restituito non è stato qualificato con lo **\[ \_ stato \] di comunicazione** o gli attributi di **\[ \_ stato \] di errore** , il parametro funziona come se fosse un long senza segno.</span><span class="sxs-lookup"><span data-stu-id="f1026-127">If the parameter or return type was not qualified with the **\[comm\_status\]** or **\[fault\_status\]** attributes, then the parameter operates as though it were an unsigned long.</span></span>

<span data-ttu-id="f1026-128">A partire dalla versione 2,0, il compilatore MIDL genera stub che contengono l'architettura di gestione degli errori corretta.</span><span class="sxs-lookup"><span data-stu-id="f1026-128">Beginning with version 2.0, the MIDL compiler generates stubs that contain the proper error handling architecture.</span></span> <span data-ttu-id="f1026-129">Tuttavia, le versioni precedenti del compilatore MIDL gestivano un parametro o un tipo restituito di **stato di errore \_ \_ t** come se **\[** fossero stati applicati lo [**\_ stato di comunicazione**](comm-status.md) **\]** e gli attributi di **\[** [**\_ stato**](fault-status.md) di errore **\]** , anche se non erano.</span><span class="sxs-lookup"><span data-stu-id="f1026-129">However, earlier versions of the MIDL compiler handled a parameter or return type of **error\_status\_t** as though the **\[**[**comm\_status**](comm-status.md)**\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes were applied, even if they were not.</span></span> <span data-ttu-id="f1026-130">Con MIDL 2,0 o versione successiva, è necessario applicare in modo esplicito gli attributi **\[ \_ stato \] di comunicazione** e **\[ \_ stato \] di errore** al parametro o alla routine in ACF.</span><span class="sxs-lookup"><span data-stu-id="f1026-130">With MIDL 2.0 or later, you must explicitly apply the **\[comm\_status\]** and **\[fault\_status\]** attributes to the parameter or procedure in the ACF.</span></span>

<span data-ttu-id="f1026-131">Il tipo di **stato di errore \_ \_ t** è uno dei tipi predefiniti del linguaggio di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f1026-131">The **error\_status\_t** type is one of the predefined types of the interface definition language.</span></span> <span data-ttu-id="f1026-132">I tipi predefiniti possono apparire come identificatori di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come gli identificatori di tipo Function-return-type o come parametri di tipo).</span><span class="sxs-lookup"><span data-stu-id="f1026-132">Predefined types can appear as type specifiers in [**typedef**](typedef.md) declarations, in general declarations, and in function declarators (either as the function-return-type or as parameter-type specifiers).</span></span>

## <a name="see-also"></a><span data-ttu-id="f1026-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1026-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1026-134">**stato di comunicazione \_**</span><span class="sxs-lookup"><span data-stu-id="f1026-134">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="f1026-135">**stato di errore \_**</span><span class="sxs-lookup"><span data-stu-id="f1026-135">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="f1026-136">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="f1026-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f1026-137">**long**</span><span class="sxs-lookup"><span data-stu-id="f1026-137">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="f1026-138">**out**</span><span class="sxs-lookup"><span data-stu-id="f1026-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f1026-139">**typedef**</span><span class="sxs-lookup"><span data-stu-id="f1026-139">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="f1026-140">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="f1026-140">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




