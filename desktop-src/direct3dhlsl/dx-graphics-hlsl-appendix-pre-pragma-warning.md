---
title: Warning (direttiva pragma)
description: Direttiva pragma che modifica il comportamento dei messaggi di avviso del compilatore.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- Direttiva pragma warning HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955952"
---
# <a name="warning-pragma-directive"></a><span data-ttu-id="d6c5b-104">Warning (direttiva pragma)</span><span class="sxs-lookup"><span data-stu-id="d6c5b-104">warning pragma Directive</span></span>

<span data-ttu-id="d6c5b-105">Direttiva pragma che modifica il comportamento dei messaggi di avviso del compilatore.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-105">Pragma directive that modifies the behavior of compiler warning messages.</span></span>



| <span data-ttu-id="d6c5b-106">\#avviso pragma ( *warning-specifier* : *warning-number-list* \[ ; *avviso-identificatore* : *Avviso-numero-elenco*... \] )</span><span class="sxs-lookup"><span data-stu-id="d6c5b-106">\#pragma warning( *warning-specifier* : *warning-number-list* \[; *warning-specifier* : *warning-number-list*...\] )</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d6c5b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6c5b-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6c5b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d6c5b-108">Item</span></span></th>
<th><span data-ttu-id="d6c5b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6c5b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6c5b-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>avviso-identificatore</em></span><span class="sxs-lookup"><span data-stu-id="d6c5b-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-specifier</em></span></span><br/></td>
<td><span data-ttu-id="d6c5b-111">Comportamento da impostare per gli avvisi specificati.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-111">Behavior to set for the specified warnings.</span></span> <span data-ttu-id="d6c5b-112">Questo parametro può assumere uno dei valori elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d6c5b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d6c5b-113">Value</span></span></th>
<th><span data-ttu-id="d6c5b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6c5b-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6c5b-115">once</span><span class="sxs-lookup"><span data-stu-id="d6c5b-115">once</span></span></td>
<td><span data-ttu-id="d6c5b-116">Visualizza il messaggio degli avvisi con i numeri specificati una sola volta.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-116">Display the message of the warnings with the specified numbers only once.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6c5b-117">default</span><span class="sxs-lookup"><span data-stu-id="d6c5b-117">default</span></span></td>
<td><span data-ttu-id="d6c5b-118">Reimposta il comportamento degli avvisi con i numeri specificati sul valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-118">Reset the behavior of the warnings with the specified numbers to their default value.</span></span> <span data-ttu-id="d6c5b-119">Questo ha anche l'effetto di attivare un avviso che è disattivato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-119">This also has the effect of turning a warning on that is off by default.</span></span> <span data-ttu-id="d6c5b-120">L'avviso verrà generato al livello predefinito.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-120">The warning will be generated at its default level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6c5b-121">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="d6c5b-121">1, 2, 3, 4</span></span></td>
<td><span data-ttu-id="d6c5b-122">Applicare il livello specificato agli avvisi con i numeri specificati.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-122">Apply the specified level to the warnings with the specified numbers.</span></span> <span data-ttu-id="d6c5b-123">Questo ha anche l'effetto di attivare un avviso che è disattivato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-123">This also has the effect of turning a warning on that is off by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6c5b-124">disabilitare</span><span class="sxs-lookup"><span data-stu-id="d6c5b-124">disable</span></span></td>
<td><span data-ttu-id="d6c5b-125">Non emettere avvisi con i numeri specificati.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-125">Do not issue the warnings with the specified numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6c5b-126">error</span><span class="sxs-lookup"><span data-stu-id="d6c5b-126">error</span></span></td>
<td><span data-ttu-id="d6c5b-127">Segnala gli avvisi con i numeri specificati come errori.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-127">Report the warnings with the specified numbers as errors.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c5b-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>avviso-numero-elenco</em></span><span class="sxs-lookup"><span data-stu-id="d6c5b-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>warning-number-list</em></span></span></p></td>
<td><p><span data-ttu-id="d6c5b-129">Elenco delimitato da spazi vuoti dei numeri degli avvisi per i quali modificare il comportamento.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-129">White space-delimited list of the numbers of the warnings to modify the behavior of.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d6c5b-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6c5b-130">Remarks</span></span>

<span data-ttu-id="d6c5b-131">È possibile specificare un numero qualsiasi di modifiche del comportamento di avviso distinte all'interno dello stesso pragma di avviso separando le modifiche con punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-131">You can specify any number of distinct warning behavior changes within the same warning pragma by separating the changes with semicolons.</span></span>

<span data-ttu-id="d6c5b-132">Il compilatore aggiungerà 4000 a qualsiasi numero di avviso compreso tra 0 e 999.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-132">The compiler will add 4000 to any warning number that is between 0 and 999.</span></span> <span data-ttu-id="d6c5b-133">Per i numeri di avviso maggiori di 4699, (quelli associati alla generazione del codice) il pragma warning ha effetto solo se viene inserito all'esterno delle definizioni di funzione.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-133">For warning numbers greater than 4699, (those associated with code generation) the warning pragma has effect only when placed outside function definitions.</span></span> <span data-ttu-id="d6c5b-134">Il pragma viene ignorato se specifica un numero maggiore di 4699 e viene usato all'interno di una funzione.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-134">The pragma is ignored if it specifies a number greater than 4699 and is used inside a function.</span></span>

<span data-ttu-id="d6c5b-135">Il pragma warning HLSL non supporta la funzionalità **push** e **pop** del pragma warning incluso nel compilatore C++.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-135">The HLSL warning pragma does not support the **push** and **pop** functionality of the warning pragma included in the C++ compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="d6c5b-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="d6c5b-136">Examples</span></span>

<span data-ttu-id="d6c5b-137">Nell'esempio seguente vengono disabilitati gli avvisi 4507 e 4034, viene visualizzato l'avviso 4385 una volta e viene segnalato l'avviso 4164 come errore.</span><span class="sxs-lookup"><span data-stu-id="d6c5b-137">The following example disables warnings 4507 and 4034, displays warning 4385 once once, and reports warning 4164 as an error.</span></span>


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



<span data-ttu-id="d6c5b-138">L'esempio precedente è funzionalmente equivalente a quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d6c5b-138">The preceding example is functionally equivalent to the following:</span></span>


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a><span data-ttu-id="d6c5b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6c5b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c5b-140">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6c5b-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="d6c5b-141">\#pragma (direttiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6c5b-141">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





