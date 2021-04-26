---
description: Usare questa annotazione per associare un parametro dell'effetto a un controllo dell'interfaccia utente nell'ambiente host. In questo modo un utente può controllare in modo interattivo un parametro dell'effetto tramite l'applicazione host.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Annotazione dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef6af352b7dea25df34ce8a5712ad30143d6426
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998588"
---
# <a name="ui-annotation"></a>Annotazione dell'interfaccia utente

Usare questa annotazione per associare un parametro dell'effetto a un controllo dell'interfaccia utente nell'ambiente host. In questo modo un utente può controllare in modo interattivo un parametro dell'effetto tramite l'applicazione host.

DXSAS definisce un set di controlli standard in termini di modello di dati e comportamento di base che gli autori di effetti possono aspettarsi dalle applicazioni host. L'annotazione del controllo viene usata nel modo seguente:


```
string SasUiControl = "ControlType";
```



dove


```
ControlType
```



è uno dei seguenti:



| ControlType | Descrizione                                                                                                                                                                     | Tipo di dati interno                                                                                 | Annotazioni delle proprietà dei controlli                                                                                 |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Nessuno        | Non deve essere visualizzato alcun controllo. Si noti che un controllo è visibile [se SasUiVisible](#sasuivisible) è True e il tipo di controllo è di qualsiasi tipo diverso da None.                           | n/d                                                                                                | n/d                                                                                                          |
| Qualsiasi         | Ciò implica che non è richiesto alcun controllo speciale. Il controllo presentato è il risultato del comportamento definito dall'applicazione.                                                         | n/d                                                                                                | n/d                                                                                                          |
| ColorPicker | Rappresenta un valore di colore come un campione di colore. Il valore viene inserito nei componenti XYZ del vettore associato. Il componente W del vettore associato è sempre impostato su uno. | float *N* dove *N* è compreso tra 1 e 4 inclusi.                                                            | [SasUiEnum](#sasuienum)                                                                                      |
| Direzione   | Vettore di direzione.                                                                                                                                                             | float *N* dove *N* è compreso tra 2 e 4 inclusi.                                                            | Nessuno                                                                                                         |
| FilePicker  | Finestra di dialogo che consente all'utente di esplorare e selezionare un file.                                                                                                                  | string                                                                                             | Nessuno                                                                                                         |
| ListPicker  | Elenco di valori stringa da cui l'utente può selezionare una voce. I valori vengono generati [dall'annotazione SasUiEnum.](#sasuienum)                                         | Matrice di stringhe insieme a un valore intero contenente l'indice del valore stringa selezionato. | [SasUiEnum](#sasuienum)                                                                                      |
| Numerico     | Set di controlli di input numerici, ad esempio caselle di testo.                                                                                                                         | float *M* x *N dove* *M* e *N* sono da 1 a 4 inclusi.                                               | [SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiStride](#sasuistride)                                    |
| Slider      | Set di dispositivi di scorrimento.                                                                                                                                                               | float *M* x *N dove* *M* e *N* sono da 1 a 4 inclusi                                                | [SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiSteps,](#sasuisteps) [SasUiStepsPower](#sasuistepspower) |
| Stringa      | Casella di testo per la modifica del contenuto della stringa.                                                                                                                                         | string                                                                                             | Nessuno                                                                                                         |



 

Se il tipo di dati interno non è identico al tipo del parametro associato, il cast verrà eseguito quando i dati vengono trasferiti dal parametro dell'applicazione host al parametro effect.

Il valore predefinito è la stringa "None".

## <a name="ui-common-properties"></a>Proprietà comuni dell'interfaccia utente

### <a name="sasuidescription"></a>SasUiDescription

Usare questa annotazione per specificare una stringa per descrivere uno strumento. Può essere usato per gli elementi dell'interfaccia utente, ad esempio le descrizioni comandi.


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

Utilizzare questa annotazione per specificare se il parametro associato deve essere visualizzato all'utente.


```
bool SasUiVisible = false;
```



Se impostato su True, l'applicazione host deve visualizzare un controllo dell'interfaccia utente per la modifica del parametro dell'effetto annotato. Se false, nell'applicazione host non viene visualizzata alcuna interfaccia utente.

Ecco un esempio:


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



Il valore predefinito è True.

## <a name="ui-control-properties"></a>Proprietà dei controlli dell'interfaccia utente

Le annotazioni delle proprietà dei controlli sono modificatori aggiuntivi che consentono di determinare il funzionamento di un determinato controllo.

### <a name="sasuienum"></a>SasUiEnum

Questa annotazione consente di limitare l'intervallo di valori per un controllo. L'annotazione contiene una stringa di valori delimitati da virgole.

Il valore predefinito è una stringa vuota.

### <a name="sasuimax"></a>SasUiMax

Questa annotazione specifica il valore massimo del parametro associato. Può essere associato solo a un parametro di tipo numerico. Il valore massimo del parametro verrà effettivamente calcolato come:


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



PARAMETER \_ TYPE MAX è il valore massimo per il tipo utilizzato dal parametro \_ associato. Ciò significa che il valore del parametro , prendendo in considerazione [l'annotazione SasUiMax](#sasuimax) viene calcolato come:


```
ParameterValue = min(NewParameterValue, MaxValue);
```



Il valore predefinito è FLT \_ MAX, come definito in Math.h.

### <a name="sasuimin"></a>SasUiMin

Questa annotazione specifica il valore minimo del parametro associato. Può essere associato solo a qualsiasi parametro di tipo numerico. Il valore minimo del parametro verrà effettivamente calcolato come:


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



PARAMETER \_ TYPE MIN è il valore minimo per il tipo usato dal parametro \_ associato. Ciò significa che il valore del parametro , tenendo conto [dell'annotazione SasUiMin](#sasuimin) viene calcolato come:


```
ParameterValue = max(NewParameterValue, MinValue);
```



Il valore predefinito è -FLT \_ MAX come definito in Math.h.

### <a name="sasuisteps"></a>SasUiSteps

Questa annotazione specifica il numero di passaggi che è possibile usare quando si incrementa o decrementa il valore del parametro associato. L'annotazione è significativa solo per un parametro di tipo numerico. Zero specifica che l'applicazione host sceglierà un numero ragionevole di passaggi.

Il valore predefinito è 0.

### <a name="sasuistepspower"></a>SasUiStepsPower

Questa annotazione specifica l'esponente nella funzione power, che ha l'intervallo \[ 0,0f, 1,0f \] . Le applicazioni host devono implementare il metodo seguente durante il calcolo dei valori dei parametri:


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



Il valore predefinito è 1,0f.

### <a name="sasuistride"></a>SasUiStride

Questa annotazione specifica l'incremento che deve essere usato quando si incrementa o decrementa questo valore. A differenza di [SasUiSteps,](#sasuisteps) [SasUiStride](#sasuistride) è utile con un controllo casella di selezione, ad esempio, in cui i dati non sono associati e l'utente preferisce incrementare il valore del parametro per stride anziché di un numero predefinito di passaggi. Le applicazioni host devono incrementare (o decrementare a seconda del comportamento del controllo) il valore di SasUiStride come indicato di seguito:


```
ParameterValue = ParameterValue +/- SasUiStride
```



Il valore predefinito è 1,0f.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento semantico e annotazioni standard DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



