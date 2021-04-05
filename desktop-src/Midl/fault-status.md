---
title: attributo fault_status
description: L'attributo \ fault \_ status \ ACF specifica che un codice di errore di tipo Error \_ status \_ t indica un errore della procedura remota, anziché altri tipi di problemi, ad esempio gli errori di comunicazione.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- attributo fault_status MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718076"
---
# <a name="fault_status-attribute"></a><span data-ttu-id="50395-104">\_attributo stato errore</span><span class="sxs-lookup"><span data-stu-id="50395-104">fault\_status attribute</span></span>

<span data-ttu-id="50395-105">L'attributo ACF **\[ \_ dello stato \]** di errore specifica che un codice di errore di tipo [**Error \_ status \_ t**](error-status-t.md) indica un errore della procedura remota, anziché altri tipi di problemi, ad esempio gli errori di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="50395-105">The **\[fault\_status\]** ACF attribute specifies that an error code of type [**error\_status\_t**](error-status-t.md) indicates a failure of the remote procedure, rather than other types of problems such as communication errors.</span></span>

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a><span data-ttu-id="50395-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50395-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="50395-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="50395-108">Specifica zero o più attributi di funzione ACF, ad esempio **\[ \_ lo stato \] di errore** e **\[** [**NoCode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="50395-108">Specifies zero or more ACF function attributes such as **\[fault\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="50395-109">Gli attributi della funzione sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="50395-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="50395-110">Si noti che è possibile applicare zero o più attributi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="50395-110">Note that zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="50395-111">Separare più attributi di funzione con virgole.</span><span class="sxs-lookup"><span data-stu-id="50395-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="50395-112">Si noti inoltre che se **\[ \_ lo \] stato di errore** viene visualizzato come attributo di funzione, non può essere visualizzato anche come attributo di parametro.</span><span class="sxs-lookup"><span data-stu-id="50395-112">Also note that if **\[fault\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="50395-113">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="50395-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="50395-114">Specifica il nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="50395-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="50395-115">*ACF-parametri-attributi*</span><span class="sxs-lookup"><span data-stu-id="50395-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="50395-116">Specifica gli attributi che si applicano a un parametro.</span><span class="sxs-lookup"><span data-stu-id="50395-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="50395-117">Si noti che è possibile applicare zero o più attributi al parametro.</span><span class="sxs-lookup"><span data-stu-id="50395-117">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="50395-118">Gli attributi di parametro sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="50395-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="50395-119">Separare più attributi di parametro con virgole.</span><span class="sxs-lookup"><span data-stu-id="50395-119">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="50395-120">Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF.</span><span class="sxs-lookup"><span data-stu-id="50395-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="50395-121">Si noti che se **\[ \_ lo \] stato di errore** viene visualizzato come attributo di parametro, non può essere visualizzato anche come attributo di funzione.</span><span class="sxs-lookup"><span data-stu-id="50395-121">Note that if **\[fault\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="50395-122">*Nome parametro*</span><span class="sxs-lookup"><span data-stu-id="50395-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="50395-123">Specifica il parametro per la funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="50395-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="50395-124">Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="50395-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50395-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="50395-125">Remarks</span></span>

<span data-ttu-id="50395-126">L'attributo **\[ fault \_ status \]** può essere utilizzato come attributo di funzione o come attributo di parametro, ma può essere visualizzato solo una volta per ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="50395-126">The **\[fault\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="50395-127">Può essere applicato alla funzione stessa o a un parametro in ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="50395-127">It can be applied either to the function itself or to one parameter in each function.</span></span>

<span data-ttu-id="50395-128">L'attributo **\[ fault \_ status \]** può essere applicato solo a funzioni che restituiscono lo [**stato di errore del tipo \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="50395-128">The **\[fault\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="50395-129">Quando la procedura remota ha esito negativo in modo che causi la restituzione di un errore PDU, viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="50395-129">When the remote procedure fails in a way that causes a fault PDU to be returned, an error code is returned.</span></span>

<span data-ttu-id="50395-130">Quando **\[ \_ lo stato \] di errore** viene usato come attributo di parametro, il parametro deve essere un **\[** parametro [**out**](out-idl.md) **\]** di tipo [**Error \_ status \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="50395-130">When **\[fault\_status\]** is used as a parameter attribute, the parameter must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="50395-131">Se si verifica un errore del server, il parametro viene impostato sul codice di errore.</span><span class="sxs-lookup"><span data-stu-id="50395-131">If a server error occurs, the parameter is set to the error code.</span></span> <span data-ttu-id="50395-132">Quando la chiamata remota viene completata correttamente, la procedura imposta il valore.</span><span class="sxs-lookup"><span data-stu-id="50395-132">When the remote call is successfully completed, the procedure sets the value.</span></span>

<span data-ttu-id="50395-133">Non è necessario specificare il parametro associato all'attributo **\[ \_ dello stato \] di errore** nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="50395-133">The parameter associated with the **\[fault\_status\]** attribute does not have to be specified in the IDL file.</span></span> <span data-ttu-id="50395-134">Quando il parametro non viene specificato, viene generato un nuovo parametro [**out**](out-idl.md) di tipo [**Error \_ status \_ t**](error-status-t.md) dopo l'ultimo parametro definito nel file IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="50395-134">When the parameter is not specified, a new [**out**](out-idl.md) parameter of type [**error\_status\_t**](error-status-t.md) is generated following the last parameter defined in the DCE IDL file.</span></span>

<span data-ttu-id="50395-135">È possibile che lo **\[ \_ stato \] di errore** e **\[** gli attributi di [**\_ stato di comunicazione**](comm-status.md) siano **\]** visualizzati in una singola funzione, come attributi di funzione o attributi di parametro.</span><span class="sxs-lookup"><span data-stu-id="50395-135">It is possible for both the **\[fault\_status\]** and **\[**[**comm\_status**](comm-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="50395-136">Se entrambi gli attributi sono attributi di funzione o se si applicano allo stesso parametro e non si verificano errori, la funzione o il parametro presenta lo stato di errore del valore **\_ \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="50395-136">If both attributes are function attributes, or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="50395-137">In caso contrario, contiene il valore del codice di stato appropriato.</span><span class="sxs-lookup"><span data-stu-id="50395-137">Otherwise, it contains the appropriate status code value.</span></span> <span data-ttu-id="50395-138">Poiché i valori restituiti per **\[ \_ lo \] stato di errore** sono diversi dai valori restituiti per **\[ \_ lo stato \] di comunicazione**, i valori restituiti vengono immediatamente interpretati.</span><span class="sxs-lookup"><span data-stu-id="50395-138">Because values returned for **\[fault\_status\]** are different from the values returned for **\[comm\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="50395-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50395-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50395-140">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="50395-140">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="50395-141">**stato di comunicazione \_**</span><span class="sxs-lookup"><span data-stu-id="50395-141">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="50395-142">**stato di errore \_ \_ t**</span><span class="sxs-lookup"><span data-stu-id="50395-142">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="50395-143">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="50395-143">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="50395-144">**out**</span><span class="sxs-lookup"><span data-stu-id="50395-144">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




