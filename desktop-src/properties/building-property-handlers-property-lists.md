---
description: Dopo aver valutato la strategia di proprietà, è necessario determinare quali proprietà visualizzare nell'interfaccia utente di Esplora risorse e dove.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Uso degli elenchi di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967114"
---
# <a name="using-property-lists"></a>Uso degli elenchi di proprietà

Dopo aver valutato la strategia di proprietà, è necessario determinare quali proprietà visualizzare nell'interfaccia utente di Esplora risorse e dove. Sono disponibili diverse posizioni in cui le proprietà vengono visualizzate in modalità di sola lettura. La modifica delle proprietà, d'altra parte, è abilitata solo nella finestra di dialogo **Proprietà** . Questa finestra di dialogo può essere richiamata tramite il collegamento **modifica proprietà** nel **riquadro di anteprima** o il menu di scelta rapida di un elemento.

Gli elenchi di proprietà sono stringhe delimitate da punto e virgola che hanno il formato seguente.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



L'unico flag attualmente disponibile è illustrato nella tabella seguente.



| Flag | Descrizione                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | Non visualizzare la proprietà nel riquadro di **Anteprima** come indicato nel valore della chiave del registro di sistema **PreviewDetails** . Se il valore di questa proprietà non è impostato, vedere l'esempio che segue la tabella successiva. |



 

Dopo aver definito un elenco di proprietà, è possibile archiviare tale stringa nel registro di sistema tramite il sistema di [associazione file della shell](../shell/fa-file-types.md) standard nella **radice delle \_ classi HKEY \_ .** Nella tabella seguente sono riepilogati i valori per gli elenchi di proprietà che possono essere assegnati nella chiave del registro di sistema per una particolare estensione di file.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FullDetails</td>
<td>Le proprietà vengono visualizzate nella scheda <strong>Dettagli</strong> della finestra di dialogo <strong>Proprietà</strong> . Questo è l'elenco completo delle proprietà supportate dal tipo di file.</td>
</tr>
<tr class="even">
<td>PreviewDetails</td>
<td>Le proprietà vengono visualizzate nel <strong>riquadro di anteprima</strong>.</td>
</tr>
<tr class="odd">
<td>PreviewTitle</td>
<td>Le proprietà vengono visualizzate nell'area del titolo del <strong>riquadro di anteprima</strong> accanto all'anteprima dell'elemento. Il numero massimo di voci è 3. Se l'elenco di proprietà contiene un numero di dimensioni superiore al massimo consentito, il resto delle voci viene ignorato.</td>
</tr>
<tr class="even">
<td>TileInfo</td>
<td>Le proprietà vengono visualizzate quando la visualizzazione elenco è in modalità di visualizzazione <strong>riquadri</strong> . Il numero massimo di voci è 3. Se l'elenco di proprietà contiene un numero di dimensioni superiore al massimo consentito, il resto delle voci viene ignorato.
<blockquote>
[!Note]<br />
Questo valore era presente in Windows XP.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>ExtendedTileInfo</td>
<td>Le proprietà vengono visualizzate per un elemento quando la visualizzazione elenco è in modalità di visualizzazione <strong>affiancata estesa</strong> .</td>
</tr>
<tr class="even">
<td>InfoTip</td>
<td>Le proprietà vengono visualizzate in un infotip quando un utente passa il mouse su un elemento.
<blockquote>
[!Note]<br />
Questo valore era presente in Windows XP.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>QuickTip</td>
<td>Le proprietà vengono visualizzate quando è difficile recuperare le proprietà direttamente da un elemento, ad esempio quando è necessario accedere all'elemento tramite una connessione di rete lenta. È consigliabile che le proprietà denominate qui, ad esempio tipo o dimensione, non richiedano l'apertura del flusso di file per determinarne il valore.
<blockquote>
[!Note]<br />
Questo valore era presente in Windows XP.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Nell'esempio seguente viene definito il valore PreviewDetails per un tipo di file Recipe, usando un ProgID di **RecipeKey**.

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Come illustrato nell'argomento relativo all' [associazione di file della shell](../shell/fa-file-types.md) , è possibile descrivere le associazioni di file per il formato più specifico. Il formato più specifico è l'unica estensione del nome file e il modulo più generico è una chiave che si applica a tutti i file e le cartelle di file. Tra questi due estremi, è anche possibile definire un [ProgID](../shell/fa-progids.md) che raggruppa un set di estensioni di file (ad esempio, i tipi jpg e JPEG raggruppati come **jpegfile**). Quando si definiscono gli elenchi di proprietà, è necessario definirli per i ProgID oppure, in alcuni casi, estensioni di file specifiche. Evitare di basarsi su voci ampie, ad esempio la chiave **AllFileSystemObjects** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori delle proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso dei nomi dei tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
