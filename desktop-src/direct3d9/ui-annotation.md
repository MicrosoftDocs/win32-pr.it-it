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
# <a name="ui-annotation"></a>Annotazione interfaccia utente

Usare questa annotazione per associare un parametro di effetto a un controllo dell'interfaccia utente nell'ambiente host. Ciò consentirà a un utente di controllare in modo interattivo un parametro di effetto tramite l'applicazione host.

DXSAS definisce un set di controlli standard in termini di modello di dati e comportamento di base che gli autori degli effetti possono prevedere dalle applicazioni host. L'annotazione del controllo viene utilizzata come segue:


```
string SasUiControl = "ControlType";
```



dove


```
ControlType
```



è uno dei seguenti:



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| ControlType | Descrizione                                                                                                                                                                     | Tipo di dati interno                                                                                 | Annotazioni proprietà controllo                                                                                 |
| nessuno        | Nessun controllo deve essere visualizzato. Si noti che un controllo è visibile se [SasUiVisible](#sasuivisible) è true e il tipo di controllo è un tipo diverso da None.                           | n/d                                                                                                | n/d                                                                                                          |
| Qualsiasi         | Questo implica che non è richiesto alcun controllo speciale. Il controllo presentato è il risultato del comportamento definito dall'applicazione.                                                         | n/d                                                                                                | n/d                                                                                                          |
| ColorPicker | Rappresenta un valore di colore come un campione di colore. Il valore viene compresso nei componenti XYZ del vettore associato. Il componente W del vettore associato è sempre impostato su uno. | float *n* dove *N* è compreso tra 1 e 4.                                                            | [SasUiEnum](#sasuienum)                                                                                      |
| Direzione   | Vettore di direzione.                                                                                                                                                             | float *n* dove *N* è compreso tra 2 e 4.                                                            | nessuno                                                                                                         |
| Selezione file  | Finestra di dialogo che consente all'utente di individuare e selezionare un file.                                                                                                                  | string                                                                                             | nessuno                                                                                                         |
| ListPicker  | Elenco di valori stringa da cui l'utente può selezionare una voce. I valori vengono generati dall'annotazione [SasUiEnum](#sasuienum) .                                         | Matrice di stringhe insieme a un valore integer contenente l'indice del valore stringa selezionato. | [SasUiEnum](#sasuienum)                                                                                      |
| Numeric     | Set di controlli di input numerici, ad esempio caselle di testo.                                                                                                                         | float *m* x *N* dove *m* e *n* sono compresi tra 1 e 4.                                               | [SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)                                    |
| Slider      | Set di dispositivi di scorrimento.                                                                                                                                                               | float *m* x *n* dove *m* e *n* sono compresi tra 1 e 4                                                | [SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower) |
| string      | Casella di testo per la modifica del contenuto della stringa.                                                                                                                                         | string                                                                                             | nessuno                                                                                                         |



 

Se il tipo di dati interno non è identico al tipo del parametro associato, il cast verrà eseguito quando i dati vengono trasferiti dal parametro dell'applicazione host al parametro Effect.

Il valore predefinito è la stringa "None".

## <a name="ui-common-properties"></a>Proprietà comuni dell'interfaccia utente

### <a name="sasuidescription"></a>SasUiDescription

Usare questa annotazione per specificare una stringa per descrivere uno strumento. Questo può essere usato per gli elementi dell'interfaccia utente, ad esempio le descrizioni comandi.


```
string SasUiDescription = "descriptive string";
```



Ad esempio:


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



Il valore predefinito è una stringa vuota.

### <a name="sasuilabel"></a>SasUiLabel

Usare questa annotazione per specificare una stringa per etichettare qualsiasi controllo dell'interfaccia utente.


```
string SasUiLabel = "some label;
```



Ecco un esempio:


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



Il valore predefinito è una stringa vuota.

### <a name="sasuivisible"></a>SasUiVisible

Usare questa annotazione per specificare se il parametro associato deve essere visualizzato all'utente.


```
bool SasUiVisible = false;
```



Se è impostato su true, l'applicazione host deve visualizzare un controllo dell'interfaccia utente per la modifica del parametro dell'effetto annotato. Se false, non viene visualizzata alcuna interfaccia utente nell'applicazione host.

Ecco un esempio:


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



Il valore predefinito è True.

## <a name="ui-control-properties"></a>Proprietà del controllo dell'interfaccia utente

Le annotazioni delle proprietà del controllo sono modificatori aggiuntivi che consentono di determinare il funzionamento di un determinato controllo.

### <a name="sasuienum"></a>SasUiEnum

Questa annotazione consente di limitare l'intervallo di valori per un controllo. L'annotazione contiene una stringa di valori delimitati da virgole.

Il valore predefinito è una stringa vuota.

### <a name="sasuimax"></a>SasUiMax

Questa annotazione specifica il valore massimo del parametro associato. Può essere associato solo a un parametro tipizzato numericamente. Il valore massimo del parametro verrà effettivamente calcolato come:


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



Il \_ tipo \_ di parametro Max è il valore massimo per il tipo utilizzato dal parametro associato. Ciò significa che il valore del parametro, prendendo in considerazione l'annotazione [SasUiMax](#sasuimax) viene calcolato come:


```
ParameterValue = min(NewParameterValue, MaxValue);
```



Il valore predefinito è FLT \_ Max come definito in Math. h.

### <a name="sasuimin"></a>SasUiMin

Questa annotazione specifica il valore minimo del parametro associato. Può essere associato solo a un parametro tipizzato numericamente. Il valore minimo del parametro verrà effettivamente calcolato come:


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



Il \_ tipo \_ di parametro min è il valore minimo per il tipo utilizzato dal parametro associato. Ciò significa che il valore del parametro, prendendo in considerazione l'annotazione [SasUiMin](#sasuimin) viene calcolato come:


```
ParameterValue = max(NewParameterValue, MinValue);
```



Il valore predefinito è-FLT \_ Max come definito in Math. h.

### <a name="sasuisteps"></a>SasUiSteps

Questa annotazione specifica il numero di passaggi che è possibile utilizzare quando si incrementa o decrementa il valore del parametro associato. L'annotazione è significativa solo per un parametro tipizzato numericamente. Zero indica che l'applicazione host sceglierà un numero ragionevole di passaggi.

Il valore predefinito è 0.

### <a name="sasuistepspower"></a>SasUiStepsPower

Questa annotazione specifica l'esponente nella funzione Power, che ha l'intervallo \[ 0,0 f, 1.0 f \] . Quando si calcolano i valori dei parametri, le applicazioni host devono implementare il metodo seguente:


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



Il valore predefinito è 1.0 f.

### <a name="sasuistride"></a>SasUiStride

Questa annotazione specifica l'incremento da usare per incrementare o decrementare questo valore. A differenza di [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) è utile con un controllo casella di selezione, ad esempio, in cui i dati non sono associati e l'utente deve incrementare il valore del parametro in base allo stride anziché a un numero predefinito di passaggi. Le applicazioni host devono incrementare (o diminuire in base al comportamento del controllo) il valore di SasUiStride come indicato di seguito:


```
ParameterValue = ParameterValue +/- SasUiStride
```



Il valore predefinito è 1.0 f.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla semantica e le annotazioni standard DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



