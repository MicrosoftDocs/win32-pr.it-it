---
title: " Direttive if, elif, else e endif"
description: Direttive per il preprocessore che controllano la compilazione di parti di un file di origine.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Direttive if, elif, else e endif HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117770"
---
# <a name="if-elif-else-and-endif-directives"></a><span data-ttu-id="590e1-104">\#\#direttive if, elif, \# else e \# endif</span><span class="sxs-lookup"><span data-stu-id="590e1-104">\#if, \#elif, \#else, and \#endif Directives</span></span>

<span data-ttu-id="590e1-105">Direttive per il preprocessore che controllano la compilazione di parti di un file di origine.</span><span class="sxs-lookup"><span data-stu-id="590e1-105">Preprocessor directives that control compilation of portions of a source file.</span></span>



| <span data-ttu-id="590e1-106">\#Se *ifCondition* ...</span><span class="sxs-lookup"><span data-stu-id="590e1-106">\#if *ifCondition* ...</span></span>         |
|--------------------------------|
| <span data-ttu-id="590e1-107">\[\#Elif *elifCondition* ...\]</span><span class="sxs-lookup"><span data-stu-id="590e1-107">\[\#elif *elifCondition* ...\]</span></span> |
| <span data-ttu-id="590e1-108">\[\#altrimenti...\]</span><span class="sxs-lookup"><span data-stu-id="590e1-108">\[\#else ...\]</span></span>                 |
| <span data-ttu-id="590e1-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="590e1-109">\#endif</span></span>                        |



 

## <a name="parameters"></a><span data-ttu-id="590e1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="590e1-110">Parameters</span></span>



| <span data-ttu-id="590e1-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="590e1-111">Item</span></span>                                                                                                                                                                                                 | <span data-ttu-id="590e1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="590e1-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="590e1-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span><span class="sxs-lookup"><span data-stu-id="590e1-113"><span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*</span></span><br/>                                                                                   | <span data-ttu-id="590e1-114">Condizione primaria da valutare.</span><span class="sxs-lookup"><span data-stu-id="590e1-114">Primary condition to evaluate.</span></span> <span data-ttu-id="590e1-115">Se questo parametro restituisce un valore diverso da zero, l'intero testo tra la \# direttiva if e l'istanza successiva della \# direttiva elif, \# else o \# endif viene mantenuto nell'unità di conversione. in caso contrario, il codice sorgente successivo non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="590e1-115">If this parameter evaluates to a nonzero value, all text between this \#if directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="590e1-116">La condizione può utilizzare l'operatore del preprocessore definito per determinare se una specifica costante o macro del preprocessore è definita. Questo utilizzo è equivalente all'utilizzo della direttiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="590e1-116">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="590e1-117">Vedere la sezione Osservazioni per le restrizioni relative al valore del parametro *ifCondition* .</span><span class="sxs-lookup"><span data-stu-id="590e1-117">See the Remarks section for restrictions on the value of the *ifCondition* parameter.</span></span> <br/>                                                                                        |
| <span data-ttu-id="590e1-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="590e1-118"><span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[optional\]</span></span> <br/> | <span data-ttu-id="590e1-119">Altra condizione da valutare.</span><span class="sxs-lookup"><span data-stu-id="590e1-119">Other condition to evaluate.</span></span> <span data-ttu-id="590e1-120">Se il parametro *ifCondition* e tutte le \# direttive elif precedenti restituiscono zero e questo parametro restituisce un valore diverso da zero, tutto il testo tra la \# direttiva elif e l'istanza successiva della \# direttiva elif, \# else o \# endif verrà mantenuto nell'unità di conversione. in caso contrario, il codice sorgente successivo non verrà mantenuto.</span><span class="sxs-lookup"><span data-stu-id="590e1-120">If the *ifCondition* parameter and all previous \#elif directives evaluate to zero, and this parameter evaluates to a nonzero value, all text between this \#elif directive and the next instance of the \#elif, \#else, or \#endif directive is retained in the translation unit; otherwise, the subsequent source code is not retained.</span></span> <br/> <span data-ttu-id="590e1-121">La condizione può utilizzare l'operatore del preprocessore definito per determinare se una specifica costante o macro del preprocessore è definita. Questo utilizzo è equivalente all'utilizzo della direttiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="590e1-121">The condition can use the preprocessor operator defined to determine whether a specific preprocessor constant or macro is defined; this usage is equivalent to the use of the [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) directive.</span></span> <br/> <span data-ttu-id="590e1-122">Vedere la sezione Osservazioni per le restrizioni relative al valore del parametro *elifCondition* .</span><span class="sxs-lookup"><span data-stu-id="590e1-122">See the Remarks section for restrictions on the value of the *elifCondition* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="590e1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="590e1-123">Remarks</span></span>

<span data-ttu-id="590e1-124">Ogni \# direttiva if in un file di origine deve corrispondere a una \# direttiva endif di chiusura.</span><span class="sxs-lookup"><span data-stu-id="590e1-124">Each \#if directive in a source file must be matched by a closing \#endif directive.</span></span> <span data-ttu-id="590e1-125">È possibile visualizzare un numero qualsiasi di \# direttive elif tra le \# \# direttive if e endif, ma \# è consentita al massimo una direttiva else.</span><span class="sxs-lookup"><span data-stu-id="590e1-125">Any number of \#elif directives can appear between the \#if and \#endif directives, but at most one \#else directive is allowed.</span></span> <span data-ttu-id="590e1-126">La \# direttiva else, se presente, deve essere l'ultima direttiva prima di \# endif.</span><span class="sxs-lookup"><span data-stu-id="590e1-126">The \#else directive, if present, must be the last directive before \#endif.</span></span> <span data-ttu-id="590e1-127">Le direttive di compilazione condizionale contenute nei file di inclusione devono soddisfare le stesse condizioni.</span><span class="sxs-lookup"><span data-stu-id="590e1-127">Conditional-compilation directives contained in include files must satisfy the same conditions.</span></span>

<span data-ttu-id="590e1-128">Le \# \# direttive if, elif, \# else e \# endif possono annidarsi nelle parti di testo di altre \# direttive if.</span><span class="sxs-lookup"><span data-stu-id="590e1-128">The \#if, \#elif, \#else, and \#endif directives can nest in the text portions of other \#if directives.</span></span> <span data-ttu-id="590e1-129">Ogni \# direttiva else, \# elif o endif annidata \# appartiene alla direttiva If precedente più vicina \# .</span><span class="sxs-lookup"><span data-stu-id="590e1-129">Each nested \#else, \#elif, or \#endif directive belongs to the closest preceding \#if directive.</span></span>

<span data-ttu-id="590e1-130">Se nessuna condizione restituisce un valore diverso da zero, il preprocessore seleziona il blocco di testo dopo la \# direttiva else.</span><span class="sxs-lookup"><span data-stu-id="590e1-130">If no conditions evaluate to a nonzero value, the preprocessor selects the text block after the \#else directive.</span></span> <span data-ttu-id="590e1-131">Se la \# clausola Else viene omessa e nessuna condizione restituisce un valore diverso da zero, non viene selezionato alcun blocco di testo.</span><span class="sxs-lookup"><span data-stu-id="590e1-131">If the \#else clause is omitted and no conditions evaluate to a nonzero value, no text block is selected.</span></span>

<span data-ttu-id="590e1-132">I parametri *ifCondition* e *elifCondition* soddisfano i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="590e1-132">The *ifCondition* and *elifCondition* parameters much meet the following requirements:</span></span>

-   <span data-ttu-id="590e1-133">Le espressioni di compilazione condizionale vengono considerate come valori [**Long con segno**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) e queste espressioni vengono valutate utilizzando le stesse regole delle espressioni in C++.</span><span class="sxs-lookup"><span data-stu-id="590e1-133">Conditional compilation expressions are treated as [**signed long**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) values, and these expressions are evaluated using the same rules as expressions in C++.</span></span>
-   <span data-ttu-id="590e1-134">Le espressioni devono disporre di un tipo integrale e possono includere solo costanti Integer, costanti carattere e l'operatore defined.</span><span class="sxs-lookup"><span data-stu-id="590e1-134">Expressions must have integral type and can include only integer constants, character constants, and the defined operator.</span></span>
-   <span data-ttu-id="590e1-135">Le espressioni non possono usare **sizeof** o un operatore di cast di tipo.</span><span class="sxs-lookup"><span data-stu-id="590e1-135">Expressions cannot use **sizeof** or a type-cast operator.</span></span>
-   <span data-ttu-id="590e1-136">È possibile che l'ambiente di destinazione non sia in grado di rappresentare tutti gli intervalli di Integer.</span><span class="sxs-lookup"><span data-stu-id="590e1-136">The target environment may not be able to represent all ranges of integers.</span></span>
-   <span data-ttu-id="590e1-137">La traduzione rappresenta il tipo [**int**](/windows/desktop/WinProg/windows-data-types) allo stesso modo del tipo **Long** e [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) equivale a **unsigned long**.</span><span class="sxs-lookup"><span data-stu-id="590e1-137">The translation represents type [**int**](/windows/desktop/WinProg/windows-data-types) the same as type **long**, and [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) the same as **unsigned long**.</span></span>
-   <span data-ttu-id="590e1-138">Il convertitore può traslare le costanti carattere in un set di valori di codice diverso dal set per l'ambiente di destinazione.</span><span class="sxs-lookup"><span data-stu-id="590e1-138">The translator can translate character constants to a set of code values different from the set for the target environment.</span></span> <span data-ttu-id="590e1-139">Per determinare le proprietà dell'ambiente di destinazione, verificare i valori delle macro da LIMITS.H in un'applicazione sviluppata per l'ambiente di destinazione.</span><span class="sxs-lookup"><span data-stu-id="590e1-139">To determine the properties of the target environment, check values of macros from LIMITS.H in an application built for the target environment.</span></span>
-   <span data-ttu-id="590e1-140">L'espressione non deve eseguire alcuna analisi di ambiente e deve rimanere isolata dai dettagli di implementazione nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="590e1-140">The expression must not perform any environmental inquiries and must remain insulated from implementation details on the target computer.</span></span>

## <a name="examples"></a><span data-ttu-id="590e1-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="590e1-141">Examples</span></span>

<span data-ttu-id="590e1-142">Questa sezione contiene esempi che illustrano come usare le direttive per il preprocessore di compilazione condizionale.</span><span class="sxs-lookup"><span data-stu-id="590e1-142">This section contains examples that demonstrate how to use conditional compilation preprocessor directives.</span></span>

### <a name="use-of-the-defined-operator"></a><span data-ttu-id="590e1-143">Utilizzo dell'operatore definito</span><span class="sxs-lookup"><span data-stu-id="590e1-143">Use of the defined operator</span></span>

<span data-ttu-id="590e1-144">Nell'esempio seguente viene illustrato l'utilizzo dell'operatore definito.</span><span class="sxs-lookup"><span data-stu-id="590e1-144">The following example shows the use of the defined operator.</span></span> <span data-ttu-id="590e1-145">Se viene definito il credito dell'identificatore, viene compilata la chiamata alla funzione di **credito** .</span><span class="sxs-lookup"><span data-stu-id="590e1-145">If the identifier CREDIT is defined, the call to the **credit** function is compiled.</span></span> <span data-ttu-id="590e1-146">Se viene definito il debito dell'identificatore, viene compilata la chiamata alla funzione di **debito** .</span><span class="sxs-lookup"><span data-stu-id="590e1-146">If the identifier DEBIT is defined, the call to the **debit** function is compiled.</span></span> <span data-ttu-id="590e1-147">Se non viene definito alcun identificatore, viene compilata la chiamata alla funzione **printerror** .</span><span class="sxs-lookup"><span data-stu-id="590e1-147">If neither identifier is defined, the call to the **printerror** function is compiled.</span></span> <span data-ttu-id="590e1-148">Si noti che "CREDIT" e "Credit" sono identificatori distinti in C e C++ perché i casi sono diversi.</span><span class="sxs-lookup"><span data-stu-id="590e1-148">Note that "CREDIT" and "credit" are distinct identifiers in C and C++ because their cases are different.</span></span>


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a><span data-ttu-id="590e1-149">Uso delle \# direttive if annidate</span><span class="sxs-lookup"><span data-stu-id="590e1-149">Use of nested \#if directives</span></span>

<span data-ttu-id="590e1-150">Nell'esempio seguente viene illustrato come annidare le \# direttive if.</span><span class="sxs-lookup"><span data-stu-id="590e1-150">The following example shows how to nest \#if directives.</span></span> <span data-ttu-id="590e1-151">In questo esempio si presuppone che sia stata definita in precedenza una costante simbolica denominata DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="590e1-151">This example assumes that a symbolic constant named DLEVEL has been previously defined.</span></span> <span data-ttu-id="590e1-152">Le \# \# direttive elif e else vengono usate per effettuare una delle quattro scelte, in base al valore di DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="590e1-152">The \#elif and \#else directives are used to make one of four choices, based on the value of DLEVEL.</span></span> <span data-ttu-id="590e1-153">Lo STACK di costanti è impostato su 0, 100 o 200, a seconda della definizione di DLEVEL.</span><span class="sxs-lookup"><span data-stu-id="590e1-153">The constant STACK is set to 0, 100, or 200, depending on the definition of DLEVEL.</span></span> <span data-ttu-id="590e1-154">Se DLEVEL è maggiore di 5, STACK non è definito.</span><span class="sxs-lookup"><span data-stu-id="590e1-154">If DLEVEL is greater than 5, then STACK is not defined.</span></span>


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a><span data-ttu-id="590e1-155">Usare per includere i file di intestazione</span><span class="sxs-lookup"><span data-stu-id="590e1-155">Use for including header files</span></span>

<span data-ttu-id="590e1-156">Generalmente la compilazione condizionale viene utilizzata per evitare più inclusioni dello stesso file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="590e1-156">A common use for conditional compilation is to prevent multiple inclusions of the same header file.</span></span> <span data-ttu-id="590e1-157">In C++, in cui le classi sono spesso definite in file di intestazione, è possibile usare costrutti di compilazione condizionale per impedire più definizioni.</span><span class="sxs-lookup"><span data-stu-id="590e1-157">In C++, where classes are often defined in header files, conditional compilation constructs can be used to prevent multiple definitions.</span></span> <span data-ttu-id="590e1-158">Nell'esempio seguente viene determinato se è definita la costante simbolica di esempio \_ H.</span><span class="sxs-lookup"><span data-stu-id="590e1-158">The following example determines whether the symbolic constant EXAMPLE\_H is defined.</span></span> <span data-ttu-id="590e1-159">In tal caso, il file è già stato incluso e non deve essere rielaborato; in caso contrario, \_ viene definita la costante di esempio H per indicare l'esempio. H è già stato elaborato.</span><span class="sxs-lookup"><span data-stu-id="590e1-159">If so, the file has already been included and does not need to be reprocessed; if not, the constant EXAMPLE\_H is defined to indicate that EXAMPLE.H has already been processed.</span></span>


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a><span data-ttu-id="590e1-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="590e1-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="590e1-161">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="590e1-161">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

