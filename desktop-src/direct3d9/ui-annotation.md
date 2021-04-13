---
description: Usare questa annotazione per associare un parametro di effetto a un controllo dell'interfaccia utente nell'ambiente host. Ciò consentirà a un utente di controllare in modo interattivo un parametro di effetto tramite l'applicazione host.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Annotazione interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e873c83a01c5c2214cb49a93e75167e58a3389
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482677"
---
# <a name="ui-annotation"></a><span data-ttu-id="2b13a-104">Annotazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="2b13a-104">UI Annotation</span></span>

<span data-ttu-id="2b13a-105">Usare questa annotazione per associare un parametro di effetto a un controllo dell'interfaccia utente nell'ambiente host.</span><span class="sxs-lookup"><span data-stu-id="2b13a-105">Use this annotation to associate an effect parameter with a UI control in the host environment.</span></span> <span data-ttu-id="2b13a-106">Ciò consentirà a un utente di controllare in modo interattivo un parametro di effetto tramite l'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="2b13a-106">This will allow a user to interactively control an effect parameter through the host application.</span></span>

<span data-ttu-id="2b13a-107">DXSAS definisce un set di controlli standard in termini di modello di dati e comportamento di base che gli autori degli effetti possono prevedere dalle applicazioni host.</span><span class="sxs-lookup"><span data-stu-id="2b13a-107">DXSAS defines a set of standard controls in terms of the data model and basic behavior that effect authors can expect from host applications.</span></span> <span data-ttu-id="2b13a-108">L'annotazione del controllo viene utilizzata come segue:</span><span class="sxs-lookup"><span data-stu-id="2b13a-108">The control annotation is used like this:</span></span>


```
string SasUiControl = "ControlType";
```



<span data-ttu-id="2b13a-109">dove</span><span class="sxs-lookup"><span data-stu-id="2b13a-109">where</span></span>


```
ControlType
```



<span data-ttu-id="2b13a-110">è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b13a-110">is one of the following:</span></span>



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b13a-111">ControlType</span><span class="sxs-lookup"><span data-stu-id="2b13a-111">ControlType</span></span> | <span data-ttu-id="2b13a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b13a-112">Description</span></span>                                                                                                                                                                     | <span data-ttu-id="2b13a-113">Tipo di dati interno</span><span class="sxs-lookup"><span data-stu-id="2b13a-113">Internal Data Type</span></span>                                                                                 | <span data-ttu-id="2b13a-114">Annotazioni proprietà controllo</span><span class="sxs-lookup"><span data-stu-id="2b13a-114">Control Property Annotations</span></span>                                                                                 |
| <span data-ttu-id="2b13a-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b13a-115">None</span></span>        | <span data-ttu-id="2b13a-116">Nessun controllo deve essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-116">No control should be shown.</span></span> <span data-ttu-id="2b13a-117">Si noti che un controllo è visibile se [SasUiVisible](#sasuivisible) è true e il tipo di controllo è un tipo diverso da None.</span><span class="sxs-lookup"><span data-stu-id="2b13a-117">Note that a control is visible if [SasUiVisible](#sasuivisible) is True and the control type is any type other than None.</span></span>                           | <span data-ttu-id="2b13a-118">n/d</span><span class="sxs-lookup"><span data-stu-id="2b13a-118">n/a</span></span>                                                                                                | <span data-ttu-id="2b13a-119">n/d</span><span class="sxs-lookup"><span data-stu-id="2b13a-119">n/a</span></span>                                                                                                          |
| <span data-ttu-id="2b13a-120">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="2b13a-120">Any</span></span>         | <span data-ttu-id="2b13a-121">Questo implica che non è richiesto alcun controllo speciale.</span><span class="sxs-lookup"><span data-stu-id="2b13a-121">This implies that no special control is requested.</span></span> <span data-ttu-id="2b13a-122">Il controllo presentato è il risultato del comportamento definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b13a-122">The control presented is the result of application-defined behavior.</span></span>                                                         | <span data-ttu-id="2b13a-123">n/d</span><span class="sxs-lookup"><span data-stu-id="2b13a-123">n/a</span></span>                                                                                                | <span data-ttu-id="2b13a-124">n/d</span><span class="sxs-lookup"><span data-stu-id="2b13a-124">n/a</span></span>                                                                                                          |
| <span data-ttu-id="2b13a-125">ColorPicker</span><span class="sxs-lookup"><span data-stu-id="2b13a-125">ColorPicker</span></span> | <span data-ttu-id="2b13a-126">Rappresenta un valore di colore come un campione di colore.</span><span class="sxs-lookup"><span data-stu-id="2b13a-126">Represent a color value as a color swatch.</span></span> <span data-ttu-id="2b13a-127">Il valore viene compresso nei componenti XYZ del vettore associato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-127">The value is packed into the XYZ components of the associated vector.</span></span> <span data-ttu-id="2b13a-128">Il componente W del vettore associato è sempre impostato su uno.</span><span class="sxs-lookup"><span data-stu-id="2b13a-128">The W component of the associated vector is always set to one.</span></span> | <span data-ttu-id="2b13a-129">float *n* dove *N* è compreso tra 1 e 4.</span><span class="sxs-lookup"><span data-stu-id="2b13a-129">float *N* where *N* is 1 to 4 inclusive.</span></span>                                                            | [<span data-ttu-id="2b13a-130">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="2b13a-130">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="2b13a-131">Direzione</span><span class="sxs-lookup"><span data-stu-id="2b13a-131">Direction</span></span>   | <span data-ttu-id="2b13a-132">Vettore di direzione.</span><span class="sxs-lookup"><span data-stu-id="2b13a-132">A direction vector.</span></span>                                                                                                                                                             | <span data-ttu-id="2b13a-133">float *n* dove *N* è compreso tra 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="2b13a-133">float *N* where *N* is 2 to 4 inclusive.</span></span>                                                            | <span data-ttu-id="2b13a-134">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b13a-134">None</span></span>                                                                                                         |
| <span data-ttu-id="2b13a-135">Selezione file</span><span class="sxs-lookup"><span data-stu-id="2b13a-135">FilePicker</span></span>  | <span data-ttu-id="2b13a-136">Finestra di dialogo che consente all'utente di individuare e selezionare un file.</span><span class="sxs-lookup"><span data-stu-id="2b13a-136">A dialog box that allows the user to browse and select a file.</span></span>                                                                                                                  | <span data-ttu-id="2b13a-137">string</span><span class="sxs-lookup"><span data-stu-id="2b13a-137">string</span></span>                                                                                             | <span data-ttu-id="2b13a-138">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b13a-138">None</span></span>                                                                                                         |
| <span data-ttu-id="2b13a-139">ListPicker</span><span class="sxs-lookup"><span data-stu-id="2b13a-139">ListPicker</span></span>  | <span data-ttu-id="2b13a-140">Elenco di valori stringa da cui l'utente può selezionare una voce.</span><span class="sxs-lookup"><span data-stu-id="2b13a-140">A list of string values from which the user can select one entry.</span></span> <span data-ttu-id="2b13a-141">I valori vengono generati dall'annotazione [SasUiEnum](#sasuienum) .</span><span class="sxs-lookup"><span data-stu-id="2b13a-141">The values are generated from the [SasUiEnum](#sasuienum) annotation.</span></span>                                         | <span data-ttu-id="2b13a-142">Matrice di stringhe insieme a un valore integer contenente l'indice del valore stringa selezionato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-142">An array of strings along with an integer value containing the index of the selected string value.</span></span> | [<span data-ttu-id="2b13a-143">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="2b13a-143">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="2b13a-144">Numeric</span><span class="sxs-lookup"><span data-stu-id="2b13a-144">Numeric</span></span>     | <span data-ttu-id="2b13a-145">Set di controlli di input numerici, ad esempio caselle di testo.</span><span class="sxs-lookup"><span data-stu-id="2b13a-145">A set of numerical input controls (such as text boxes).</span></span>                                                                                                                         | <span data-ttu-id="2b13a-146">float *m* x *N* dove *m* e *n* sono compresi tra 1 e 4.</span><span class="sxs-lookup"><span data-stu-id="2b13a-146">float *M* x *N* where *M* and *N* are 1 to 4 inclusive.</span></span>                                               | <span data-ttu-id="2b13a-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span><span class="sxs-lookup"><span data-stu-id="2b13a-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span></span>                                    |
| <span data-ttu-id="2b13a-148">Slider</span><span class="sxs-lookup"><span data-stu-id="2b13a-148">Slider</span></span>      | <span data-ttu-id="2b13a-149">Set di dispositivi di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="2b13a-149">A set of sliders.</span></span>                                                                                                                                                               | <span data-ttu-id="2b13a-150">float *m* x *n* dove *m* e *n* sono compresi tra 1 e 4</span><span class="sxs-lookup"><span data-stu-id="2b13a-150">float *M* x *N* where *M* and *N* are 1 to 4 inclusive</span></span>                                                | <span data-ttu-id="2b13a-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span><span class="sxs-lookup"><span data-stu-id="2b13a-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span></span> |
| <span data-ttu-id="2b13a-152">string</span><span class="sxs-lookup"><span data-stu-id="2b13a-152">String</span></span>      | <span data-ttu-id="2b13a-153">Casella di testo per la modifica del contenuto della stringa.</span><span class="sxs-lookup"><span data-stu-id="2b13a-153">An text box for editing string content.</span></span>                                                                                                                                         | <span data-ttu-id="2b13a-154">string</span><span class="sxs-lookup"><span data-stu-id="2b13a-154">string</span></span>                                                                                             | <span data-ttu-id="2b13a-155">nessuno</span><span class="sxs-lookup"><span data-stu-id="2b13a-155">None</span></span>                                                                                                         |



 

<span data-ttu-id="2b13a-156">Se il tipo di dati interno non è identico al tipo del parametro associato, il cast verrà eseguito quando i dati vengono trasferiti dal parametro dell'applicazione host al parametro Effect.</span><span class="sxs-lookup"><span data-stu-id="2b13a-156">If the internal data type is not identical to the associated parameter's type, casting will occur when data is transferred from the host application parameter to the effect parameter.</span></span>

<span data-ttu-id="2b13a-157">Il valore predefinito è la stringa "None".</span><span class="sxs-lookup"><span data-stu-id="2b13a-157">The default is the string "None".</span></span>

## <a name="ui-common-properties"></a><span data-ttu-id="2b13a-158">Proprietà comuni dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="2b13a-158">UI Common Properties</span></span>

### <a name="sasuidescription"></a><span data-ttu-id="2b13a-159">SasUiDescription</span><span class="sxs-lookup"><span data-stu-id="2b13a-159">SasUiDescription</span></span>

<span data-ttu-id="2b13a-160">Usare questa annotazione per specificare una stringa per descrivere uno strumento.</span><span class="sxs-lookup"><span data-stu-id="2b13a-160">Use this annotation to specify a string to describe a tool.</span></span> <span data-ttu-id="2b13a-161">Questo può essere usato per gli elementi dell'interfaccia utente, ad esempio le descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="2b13a-161">This could be used for UI elements such as tool tips.</span></span>


```
string SasUiDescription = "descriptive string";
```



<span data-ttu-id="2b13a-162">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2b13a-162">For instance:</span></span>


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



<span data-ttu-id="2b13a-163">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="2b13a-163">The default is an empty string.</span></span>

### <a name="sasuilabel"></a><span data-ttu-id="2b13a-164">SasUiLabel</span><span class="sxs-lookup"><span data-stu-id="2b13a-164">SasUiLabel</span></span>

<span data-ttu-id="2b13a-165">Usare questa annotazione per specificare una stringa per etichettare qualsiasi controllo dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2b13a-165">Use this annotation to specify a string to label any UI control.</span></span>


```
string SasUiLabel = "some label;
```



<span data-ttu-id="2b13a-166">Ecco un esempio:</span><span class="sxs-lookup"><span data-stu-id="2b13a-166">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



<span data-ttu-id="2b13a-167">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="2b13a-167">The default is an empty string.</span></span>

### <a name="sasuivisible"></a><span data-ttu-id="2b13a-168">SasUiVisible</span><span class="sxs-lookup"><span data-stu-id="2b13a-168">SasUiVisible</span></span>

<span data-ttu-id="2b13a-169">Usare questa annotazione per specificare se il parametro associato deve essere visualizzato all'utente.</span><span class="sxs-lookup"><span data-stu-id="2b13a-169">Use this annotation to specify whether the associated parameter should be displayed to the user.</span></span>


```
bool SasUiVisible = false;
```



<span data-ttu-id="2b13a-170">Se è impostato su true, l'applicazione host deve visualizzare un controllo dell'interfaccia utente per la modifica del parametro dell'effetto annotato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-170">If set to True, the host application should display a UI control for editing the annotated effect parameter.</span></span> <span data-ttu-id="2b13a-171">Se false, non viene visualizzata alcuna interfaccia utente nell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="2b13a-171">If false, no UI is displayed in the host application.</span></span>

<span data-ttu-id="2b13a-172">Ecco un esempio:</span><span class="sxs-lookup"><span data-stu-id="2b13a-172">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



<span data-ttu-id="2b13a-173">Il valore predefinito è True.</span><span class="sxs-lookup"><span data-stu-id="2b13a-173">The default is True.</span></span>

## <a name="ui-control-properties"></a><span data-ttu-id="2b13a-174">Proprietà del controllo dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="2b13a-174">UI Control Properties</span></span>

<span data-ttu-id="2b13a-175">Le annotazioni delle proprietà del controllo sono modificatori aggiuntivi che consentono di determinare il funzionamento di un determinato controllo.</span><span class="sxs-lookup"><span data-stu-id="2b13a-175">Control property annotations are additional modifiers that help determine how a particular control operates.</span></span>

### <a name="sasuienum"></a><span data-ttu-id="2b13a-176">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="2b13a-176">SasUiEnum</span></span>

<span data-ttu-id="2b13a-177">Questa annotazione consente di limitare l'intervallo di valori per un controllo.</span><span class="sxs-lookup"><span data-stu-id="2b13a-177">This annotation allows you to restrict the range of values for a control.</span></span> <span data-ttu-id="2b13a-178">L'annotazione contiene una stringa di valori delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="2b13a-178">The annotation contains a string of values delimited by commas.</span></span>

<span data-ttu-id="2b13a-179">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="2b13a-179">The default is an empty string.</span></span>

### <a name="sasuimax"></a><span data-ttu-id="2b13a-180">SasUiMax</span><span class="sxs-lookup"><span data-stu-id="2b13a-180">SasUiMax</span></span>

<span data-ttu-id="2b13a-181">Questa annotazione specifica il valore massimo del parametro associato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-181">This annotation specifies the maximum value of the associated parameter.</span></span> <span data-ttu-id="2b13a-182">Può essere associato solo a un parametro tipizzato numericamente.</span><span class="sxs-lookup"><span data-stu-id="2b13a-182">It can only be associated with a numerically-typed parameter.</span></span> <span data-ttu-id="2b13a-183">Il valore massimo del parametro verrà effettivamente calcolato come:</span><span class="sxs-lookup"><span data-stu-id="2b13a-183">The maximum value of the parameter will actually be calculated as:</span></span>


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



<span data-ttu-id="2b13a-184">Il \_ tipo \_ di parametro Max è il valore massimo per il tipo utilizzato dal parametro associato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-184">PARAMETER\_TYPE\_MAX is the maximum value for the type used by the associated parameter.</span></span> <span data-ttu-id="2b13a-185">Ciò significa che il valore del parametro, prendendo in considerazione l'annotazione [SasUiMax](#sasuimax) viene calcolato come:</span><span class="sxs-lookup"><span data-stu-id="2b13a-185">This means that the value of the parameter, taking into account the [SasUiMax](#sasuimax) annotation is calculated as:</span></span>


```
ParameterValue = min(NewParameterValue, MaxValue);
```



<span data-ttu-id="2b13a-186">Il valore predefinito è FLT \_ Max come definito in Math. h.</span><span class="sxs-lookup"><span data-stu-id="2b13a-186">The default value is FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuimin"></a><span data-ttu-id="2b13a-187">SasUiMin</span><span class="sxs-lookup"><span data-stu-id="2b13a-187">SasUiMin</span></span>

<span data-ttu-id="2b13a-188">Questa annotazione specifica il valore minimo del parametro associato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-188">This annotation specifies the minimum value of the associated parameter.</span></span> <span data-ttu-id="2b13a-189">Può essere associato solo a un parametro tipizzato numericamente.</span><span class="sxs-lookup"><span data-stu-id="2b13a-189">It can only be associated with any numerically-typed parameter.</span></span> <span data-ttu-id="2b13a-190">Il valore minimo del parametro verrà effettivamente calcolato come:</span><span class="sxs-lookup"><span data-stu-id="2b13a-190">The minimum value of the parameter will actually be calculated as:</span></span>


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



<span data-ttu-id="2b13a-191">Il \_ tipo \_ di parametro min è il valore minimo per il tipo utilizzato dal parametro associato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-191">PARAMETER\_TYPE\_MIN is the minimum value for the type used by the associated parameter.</span></span> <span data-ttu-id="2b13a-192">Ciò significa che il valore del parametro, prendendo in considerazione l'annotazione [SasUiMin](#sasuimin) viene calcolato come:</span><span class="sxs-lookup"><span data-stu-id="2b13a-192">This means that the value of the parameter, taking into account the [SasUiMin](#sasuimin) annotation is calculated as:</span></span>


```
ParameterValue = max(NewParameterValue, MinValue);
```



<span data-ttu-id="2b13a-193">Il valore predefinito è-FLT \_ Max come definito in Math. h.</span><span class="sxs-lookup"><span data-stu-id="2b13a-193">The default value is -FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuisteps"></a><span data-ttu-id="2b13a-194">SasUiSteps</span><span class="sxs-lookup"><span data-stu-id="2b13a-194">SasUiSteps</span></span>

<span data-ttu-id="2b13a-195">Questa annotazione specifica il numero di passaggi che è possibile utilizzare quando si incrementa o decrementa il valore del parametro associato.</span><span class="sxs-lookup"><span data-stu-id="2b13a-195">This annotation specifies the number of steps that can be used when incrementing or decrementing the associated parameter value.</span></span> <span data-ttu-id="2b13a-196">L'annotazione è significativa solo per un parametro tipizzato numericamente.</span><span class="sxs-lookup"><span data-stu-id="2b13a-196">The annotation is only meaningful on a numerically-typed parameter.</span></span> <span data-ttu-id="2b13a-197">Zero indica che l'applicazione host sceglierà un numero ragionevole di passaggi.</span><span class="sxs-lookup"><span data-stu-id="2b13a-197">Zero specifies that the host application will choose a reasonable number of steps.</span></span>

<span data-ttu-id="2b13a-198">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="2b13a-198">The default value is 0.</span></span>

### <a name="sasuistepspower"></a><span data-ttu-id="2b13a-199">SasUiStepsPower</span><span class="sxs-lookup"><span data-stu-id="2b13a-199">SasUiStepsPower</span></span>

<span data-ttu-id="2b13a-200">Questa annotazione specifica l'esponente nella funzione Power, che ha l'intervallo \[ 0,0 f, 1.0 f \] .</span><span class="sxs-lookup"><span data-stu-id="2b13a-200">This annotation specifies the exponent in the power function, which has the range \[0.0f, 1.0f\].</span></span> <span data-ttu-id="2b13a-201">Quando si calcolano i valori dei parametri, le applicazioni host devono implementare il metodo seguente:</span><span class="sxs-lookup"><span data-stu-id="2b13a-201">Host applications must implement the following method when calculating parameter values:</span></span>


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



<span data-ttu-id="2b13a-202">Il valore predefinito è 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="2b13a-202">The default value is 1.0f.</span></span>

### <a name="sasuistride"></a><span data-ttu-id="2b13a-203">SasUiStride</span><span class="sxs-lookup"><span data-stu-id="2b13a-203">SasUiStride</span></span>

<span data-ttu-id="2b13a-204">Questa annotazione specifica l'incremento da usare per incrementare o decrementare questo valore.</span><span class="sxs-lookup"><span data-stu-id="2b13a-204">This annotation specifies the increment that should be used when incrementing or decrementing this value.</span></span> <span data-ttu-id="2b13a-205">A differenza di [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) è utile con un controllo casella di selezione, ad esempio, in cui i dati non sono associati e l'utente deve incrementare il valore del parametro in base allo stride anziché a un numero predefinito di passaggi.</span><span class="sxs-lookup"><span data-stu-id="2b13a-205">Unlike [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) is useful with a spinner control, for instance, where the data is unbounded and the user would rather increment the parameter value by stride rather than by a pre-defined number of steps.</span></span> <span data-ttu-id="2b13a-206">Le applicazioni host devono incrementare (o diminuire in base al comportamento del controllo) il valore di SasUiStride come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2b13a-206">Host applications should increment (or decrement depending on the control behavior) by the value of SasUiStride as follows:</span></span>


```
ParameterValue = ParameterValue +/- SasUiStride
```



<span data-ttu-id="2b13a-207">Il valore predefinito è 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="2b13a-207">The default value is 1.0f.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b13a-208">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b13a-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b13a-209">Informazioni di riferimento sulla semantica e le annotazioni standard DirectX</span><span class="sxs-lookup"><span data-stu-id="2b13a-209">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



