---
description: Dopo aver valutato la strategia di proprietà, è necessario determinare le proprietà da visualizzare nell'interfaccia utente Windows Explorer e dove.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Uso degli elenchi di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72289612d61ebfb198ec0f2ee3d4a7d206209e91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477397"
---
# <a name="using-property-lists"></a>Uso degli elenchi di proprietà

Dopo aver valutato la strategia di proprietà, è necessario determinare le proprietà da visualizzare nell'interfaccia utente Windows Explorer e dove. Esistono diverse posizioni in cui le proprietà vengono visualizzate in modalità di sola lettura. La modifica delle proprietà, d'altra parte, è abilitata solo nella **finestra di dialogo** Proprietà. Tale finestra di dialogo può essere richiamata tramite il **collegamento** Modifica proprietà nel riquadro di **anteprima** o il menu di scelta rapida di un elemento.

Gli elenchi di proprietà sono stringhe delimitate da punto e virgola nel formato seguente.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



L'unico flag attualmente disponibile è illustrato nella tabella seguente.



| Flag | Descrizione                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | Non visualizzare la proprietà nel riquadro **di** anteprima come indicato nel valore della chiave del Registro di sistema **PreviewDetails.** Vedere l'esempio che segue la tabella seguente se il valore di tale proprietà non è impostato. |



 

Dopo aver definito un elenco di proprietà, è possibile archiviare tale stringa nel Registro di sistema tramite il [file association](../shell/fa-file-types.md) system shell standard in **HKEY CLASSES \_ \_ ROOT.** Nella tabella seguente sono riepilogati i valori per gli elenchi di proprietà che possono essere assegnati nella chiave del Registro di sistema per una determinata estensione di file.




| valore | Descrizione | 
|-------|-------------|
| Dettagli completi | Le proprietà vengono visualizzate nella <strong>scheda Dettagli</strong> della <strong>finestra di</strong> dialogo Proprietà . Questo è l'elenco completo delle proprietà supportate dal tipo di file. | 
| AnteprimaDettagli | Le proprietà vengono visualizzate nel riquadro <strong>di anteprima.</strong> | 
| PreviewTitle | Le proprietà vengono visualizzate nell'area del titolo del riquadro <strong>di anteprima</strong> accanto all'anteprima dell'elemento. Il numero massimo di voci è 3. Se l'elenco di proprietà contiene più del numero massimo consentito, le altre voci vengono ignorate. | 
| TileInfo | Le proprietà vengono visualizzate quando la visualizzazione elenco è in <strong>modalità di</strong> visualizzazione Riquadri. Il numero massimo di voci è 3. Se l'elenco di proprietà contiene più del numero massimo consentito, le altre voci vengono ignorate.<blockquote>[!Note]<br />Questo valore era presente in Windows XP.</blockquote><br /> | 
| ExtendedTileInfo | Le proprietà vengono visualizzate per un elemento quando la visualizzazione elenco è in <strong>modalità di visualizzazione Riquadro</strong> esteso. | 
| InfoTip | Le proprietà vengono visualizzate in una descrizione comando quando un utente passa il mouse su un elemento.<blockquote>[!Note]<br />Questo valore era presente in Windows XP.</blockquote><br /> | 
| Quicktip | Le proprietà vengono visualizzate quando è difficile recuperare le proprietà direttamente da un elemento, ad esempio quando è necessario accedere all'elemento tramite una connessione di rete lenta. È consigliabile che le proprietà denominate qui, ad esempio Tipo o Dimensione, non richiedano l'apertura del flusso di file per determinarne il valore.<blockquote>[!Note]<br />Questo valore era presente in Windows XP.</blockquote><br /> | 




 

L'esempio seguente definisce il valore PreviewDetails per un tipo di file recipe, usando un ProgID **di RecipeKey.**

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Come illustrato [nell'argomento Associazione di file della shell,](../shell/fa-file-types.md) le associazioni di file possono essere descritte per la forma più specifica per la forma più generale. La forma più specifica è l'unica estensione di file e la forma più generica è una chiave che si applica a tutti i file e le cartelle di file. Tra questi due estremi, è anche possibile definire un [PROGID](../shell/fa-progids.md) che raggruppa un set di estensioni di file (ad esempio, i tipi .jpg e jpeg raggruppati come **jpegfile**). Quando si definiscono elenchi di proprietà, è necessario definirli per ProgID o, in alcuni casi, estensioni di file specifiche. Evitare di basarsi su voci generali, ad esempio **la chiave AllFileSystemObjects.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui gestori di proprietà](./building-property-handlers-properties.md)
</dt> <dt>

[Uso di nomi di tipi](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Inizializzazione di gestori di proprietà](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrazione e distribuzione di gestori di proprietà](./prophand-reg-dist.md)
</dt> <dt>

[Procedure consigliate e domande frequenti sul gestore delle proprietà](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
