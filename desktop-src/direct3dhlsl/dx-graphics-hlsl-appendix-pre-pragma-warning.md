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
# <a name="warning-pragma-directive"></a>Warning (direttiva pragma)

Direttiva pragma che modifica il comportamento dei messaggi di avviso del compilatore.



| \#avviso pragma ( *warning-specifier* : *warning-number-list* \[ ; *avviso-identificatore* : *Avviso-numero-elenco*... \] ) |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parametri



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>avviso-identificatore</em><br/></td>
<td>Comportamento da impostare per gli avvisi specificati. Questo parametro può assumere uno dei valori elencati nella tabella seguente. <br/> 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>once</td>
<td>Visualizza il messaggio degli avvisi con i numeri specificati una sola volta.</td>
</tr>
<tr class="even">
<td>default</td>
<td>Reimposta il comportamento degli avvisi con i numeri specificati sul valore predefinito. Questo ha anche l'effetto di attivare un avviso che è disattivato per impostazione predefinita. L'avviso verrà generato al livello predefinito.</td>
</tr>
<tr class="odd">
<td>1, 2, 3, 4</td>
<td>Applicare il livello specificato agli avvisi con i numeri specificati. Questo ha anche l'effetto di attivare un avviso che è disattivato per impostazione predefinita.</td>
</tr>
<tr class="even">
<td>disabilitare</td>
<td>Non emettere avvisi con i numeri specificati.</td>
</tr>
<tr class="odd">
<td>error</td>
<td>Segnala gli avvisi con i numeri specificati come errori.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>avviso-numero-elenco</em></p></td>
<td><p>Elenco delimitato da spazi vuoti dei numeri degli avvisi per i quali modificare il comportamento.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

È possibile specificare un numero qualsiasi di modifiche del comportamento di avviso distinte all'interno dello stesso pragma di avviso separando le modifiche con punti e virgola.

Il compilatore aggiungerà 4000 a qualsiasi numero di avviso compreso tra 0 e 999. Per i numeri di avviso maggiori di 4699, (quelli associati alla generazione del codice) il pragma warning ha effetto solo se viene inserito all'esterno delle definizioni di funzione. Il pragma viene ignorato se specifica un numero maggiore di 4699 e viene usato all'interno di una funzione.

Il pragma warning HLSL non supporta la funzionalità **push** e **pop** del pragma warning incluso nel compilatore C++.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono disabilitati gli avvisi 4507 e 4034, viene visualizzato l'avviso 4385 una volta e viene segnalato l'avviso 4164 come errore.


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



L'esempio precedente è funzionalmente equivalente a quanto segue:


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma (direttiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





