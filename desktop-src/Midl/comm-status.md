---
title: attributo comm_status
description: L'attributo \ Comm \_ status \ ACF causa la restituzione di un codice di errore quando si verifica un errore di comunicazione durante l'esecuzione di una funzione.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- attributo comm_status MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718778"
---
# <a name="comm_status-attribute"></a><span data-ttu-id="ace1c-104">\_attributo status di comunicazione</span><span class="sxs-lookup"><span data-stu-id="ace1c-104">comm\_status attribute</span></span>

<span data-ttu-id="ace1c-105">L'attributo di **\[ \_ stato \]** di comunicazione ACF causa la restituzione di un codice di errore quando si verifica un errore di comunicazione durante l'esecuzione di una funzione.</span><span class="sxs-lookup"><span data-stu-id="ace1c-105">The **\[comm\_status\]** ACF attribute causes an error code to be returned when a communication error occurs during the execution of a function.</span></span>

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="ace1c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ace1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace1c-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="ace1c-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ace1c-108">Specifica zero o più attributi della funzione ACF, ad esempio **\[ \_ stato \] di comunicazione** e **\[** [**NoCode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ace1c-108">Specifies zero or more ACF function attributes, such as **\[comm\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="ace1c-109">Gli attributi della funzione sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="ace1c-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="ace1c-110">È possibile applicare zero o più attributi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="ace1c-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="ace1c-111">Separare più attributi di funzione con virgole.</span><span class="sxs-lookup"><span data-stu-id="ace1c-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="ace1c-112">Si noti che se **\[ \_ lo \] stato di comunicazione** viene visualizzato come attributo di funzione, non può essere visualizzato anche come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="ace1c-112">Note that if **\[comm\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ace1c-113">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="ace1c-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ace1c-114">Specifica il nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="ace1c-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="ace1c-115">*ACF-parametri-attributi*</span><span class="sxs-lookup"><span data-stu-id="ace1c-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ace1c-116">Specifica gli attributi che si applicano a un parametro.</span><span class="sxs-lookup"><span data-stu-id="ace1c-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="ace1c-117">Si noti che è possibile applicare zero, uno o più attributi al parametro.</span><span class="sxs-lookup"><span data-stu-id="ace1c-117">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="ace1c-118">Separare più attributi di parametro con virgole.</span><span class="sxs-lookup"><span data-stu-id="ace1c-118">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="ace1c-119">Gli attributi di parametro sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="ace1c-119">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="ace1c-120">Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF.</span><span class="sxs-lookup"><span data-stu-id="ace1c-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="ace1c-121">Si noti che se **\[ \_ lo \] stato di comunicazione** viene visualizzato come attributo di parametro, non può essere visualizzato anche come attributo di funzione.</span><span class="sxs-lookup"><span data-stu-id="ace1c-121">Note that if **\[comm\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ace1c-122">*Nome parametro*</span><span class="sxs-lookup"><span data-stu-id="ace1c-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ace1c-123">Specifica il parametro per la funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="ace1c-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="ace1c-124">Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="ace1c-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ace1c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ace1c-125">Remarks</span></span>

<span data-ttu-id="ace1c-126">L'attributo **\[ \_ status \] di comunicazione** può essere usato come attributo di funzione o come attributo di parametro, ma può essere visualizzato solo una volta per ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="ace1c-126">The **\[comm\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="ace1c-127">Può essere applicato alla funzione o a un parametro in ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="ace1c-127">It can be applied either to the function or to one parameter in each function.</span></span>

<span data-ttu-id="ace1c-128">L'attributo **\[ \_ status \] di comunicazione** può essere applicato solo a funzioni che restituiscono lo stato di errore del tipo [**\_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="ace1c-128">The **\[comm\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="ace1c-129">Quando si verifica un errore di comunicazione durante l'esecuzione della funzione, viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ace1c-129">When a communication error occurs during the execution of the function, an error code is returned.</span></span>

<span data-ttu-id="ace1c-130">Quando **\[ \_ lo stato \] di comunicazione** viene usato come attributo di parametro, il parametro deve essere definito nel file IDL e deve essere un **\[** parametro [**out**](out-idl.md) **\]** di tipo [**Error \_ status \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="ace1c-130">When **\[comm\_status\]** is used as a parameter attribute, the parameter must be defined in the IDL file and must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="ace1c-131">Quando si verifica un errore di comunicazione durante l'esecuzione della funzione, il parametro viene impostato sul codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ace1c-131">When a communication error occurs during the execution of the function, the parameter is set to the error code.</span></span> <span data-ttu-id="ace1c-132">Quando la chiamata remota viene completata correttamente, il valore viene impostato dalla procedura.</span><span class="sxs-lookup"><span data-stu-id="ace1c-132">When the remote call is completed successfully, the procedure sets the value.</span></span>

<span data-ttu-id="ace1c-133">È possibile che sia lo **\[ \_ \] stato di comunicazione** che **\[** gli attributi di [**\_ stato di errore**](fault-status.md) **\]** vengano visualizzati in una singola funzione, come attributi di funzione o attributi di parametro.</span><span class="sxs-lookup"><span data-stu-id="ace1c-133">It is possible for both the **\[comm\_status\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="ace1c-134">Se entrambi gli attributi sono attributi di funzione o se si applicano allo stesso parametro e non si verificano errori, la funzione o il parametro presenta lo stato di errore del valore **\_ \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ace1c-134">If both attributes are function attributes or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="ace1c-135">In caso contrario, contiene lo **\[ \_ stato \] di comunicazione** appropriato o il valore **\[ \_ dello stato \] di errore** .</span><span class="sxs-lookup"><span data-stu-id="ace1c-135">Otherwise, it contains the appropriate **\[comm\_status\]** or **\[fault\_status\]** value.</span></span> <span data-ttu-id="ace1c-136">Poiché i valori restituiti per **\[ \_ lo \] stato di comunicazione** sono diversi dai valori restituiti per **\[ \_ lo stato \] di errore**, i valori restituiti vengono immediatamente interpretati.</span><span class="sxs-lookup"><span data-stu-id="ace1c-136">Because values returned for **\[comm\_status\]** are different from the values returned for **\[fault\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="ace1c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ace1c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace1c-138">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="ace1c-138">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="ace1c-139">**stato di errore \_ \_ t**</span><span class="sxs-lookup"><span data-stu-id="ace1c-139">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="ace1c-140">**stato di errore \_**</span><span class="sxs-lookup"><span data-stu-id="ace1c-140">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="ace1c-141">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="ace1c-141">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="ace1c-142">**out**</span><span class="sxs-lookup"><span data-stu-id="ace1c-142">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




