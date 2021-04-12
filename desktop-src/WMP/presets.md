---
title: Impostazioni predefinite
description: Impostazioni predefinite
ms.assetid: fb2ccd8b-eda2-414a-870c-85b658f40eb9
keywords:
- Visualizzazioni, set di impostazioni
- Visualizzazioni personalizzate, set di impostazioni
- Visualizzazioni, set di impostazioni della barra
- Visualizzazioni personalizzate, set di impostazioni della barra
- Visualizzazioni, set di impostazioni Wave
- Visualizzazioni personalizzate, set di impostazioni Wave
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, set di impostazioni
- Visualizzazioni, funzione GetPresetTitle
- Visualizzazioni personalizzate, funzione GetPresetTitle
- GetPresetTitle (funzione)
- enumerazioni, set di impostazioni di visualizzazione
- Visualizzazioni, enumerazioni
- Visualizzazioni personalizzate, enumerazioni
- Visualizzazioni, intestazione delle risorse e stringhe
- Visualizzazioni personalizzate, intestazione delle risorse e stringhe
- set di impostazioni nelle visualizzazioni, set di impostazioni della barra
- set di impostazioni nelle visualizzazioni, set di impostazioni Wave
- set di impostazioni nelle visualizzazioni, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e024427d19da0a30f54d9ebc0590feedb8d0f97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221282"
---
# <a name="presets"></a>Impostazioni predefinite

I set di impostazioni vengono forniti come un modo per avere effetti diversi provenienti dalla stessa visualizzazione. Ad esempio, è possibile creare un effetto bagliore generato da un blocco di codice, ma usare un set di impostazioni per determinare il colore del bagliore. I nomi di set di impostazioni potrebbero essere rosso, verde e blu.

Nella procedura guidata vengono definiti due set di impostazioni per il codice generato. Una viene chiamata barre e l'altra viene chiamata Wave. Il set di impostazioni della barra Mostra le barre che mostrano l'attività nello spettro audio e usano i dati della forma d'onda. Il set di impostazioni Wave Visualizza una linea di wiggling che mostra la potenza audio della forma d'onda.

Se si modifica una qualsiasi delle informazioni del set di impostazioni, è necessario modificare anche le parti seguenti del codice generato.

## <a name="render-function"></a>Funzione render

La funzione **IWMPEffects:: Render** si trova nel file *ProjectName*. cpp, dove *NomeProgetto* è il nome del progetto scelto quando è stata eseguita la procedura guidata.

Il codice generato nella funzione **Render** usa un'istruzione switch per scegliere tra due set di impostazioni. Il set di impostazioni corrente è quello selezionato dall'utente in Windows Media Player. Se si desidera modificare il codice eseguito per un determinato set di impostazioni o aggiungere o sottrarre un set di impostazioni, modificare di conseguenza l'istruzione switch.

I due set di impostazioni sono definiti dalle **\_ barre predefinite** e dalle enumerazioni dell' **\_ ambito preimpostato** . La scelta del set di impostazioni che verrà chiamato è definita da m \_ nPreset.

## <a name="getpresettitle"></a>GetPresetTitle

La funzione **IWMPEffects:: GetPresetTitle** si trova nel file *ProjectName*. cpp, dove *NomeProgetto* è il nome del progetto scelto quando è stata eseguita la procedura guidata.

La funzione **GetPresetTitle** imposta le relazioni tra le enumerazioni predefinite e le risorse di stringa. Le barre del **set \_ di impostazioni** e l' **\_ ambito del set** di impostazioni delle enumerazioni vengono generate dalla procedura guidata e utilizzano le risorse di stringa ID \_ BARSPRESETNAME e ID \_ SCOPEPRESETNAME.

Se si aggiungono, sottraggono o si modificano i set di impostazioni, è necessario modificare le enumerazioni e le risorse di stringa.

## <a name="preset-enumerations"></a>Enumerazioni predefinite

L'enumerazione del set di impostazioni viene definita nel file *ProjectName*. h, dove *NomeProgetto* è il nome del progetto scelto quando è stata eseguita la procedura guidata.

L'enumerazione definisce i due set di impostazioni correnti e il conteggio. Se si aggiungono o si sottraggono set di impostazioni o si modifica l'enumerazione, assicurarsi di modificare questa enumerazione in modo che il numero e l'ordine dei set di impostazioni siano corretti. Questa enumerazione viene utilizzata per assicurarsi di chiamare il set di impostazioni corretto nella funzione **Render** .

## <a name="resource-header"></a>Intestazione della risorsa

È necessario impostare le risorse per i nomi del set di impostazioni nel file di intestazione Resource. h. I set di impostazioni correnti sono definiti come segue:


```C++
#define IDS_BARSPRESETNAME              102
#define IDS_SCOPEPRESETNAME             103
```



Se si aggiungono o si sottraggono set di impostazioni, è necessario modificare l'intestazione della risorsa e i relativi numeri.

## <a name="resource-strings"></a>Stringhe di risorse

I nomi effettivi dei set di impostazioni vengono definiti nel file di risorse *NomeProgetto* dll. RC, dove *NomeProgetto* è il nome del progetto scelto al momento dell'esecuzione della procedura guidata. È possibile modificare questo file manualmente oppure usare l'editor di risorse incluso in Microsoft Visual C++.

I nomi generati sono il nome della visualizzazione e il set di impostazioni specifico. Il file di risorse per il codice generato ne definirà i seguenti elementi:


```C++
IDS_BARSPRESETNAME      "projectname Bars"
IDS_SCOPEPRESETNAME     "projectname Wave"
```



dove *NomeProgetto* è il nome del progetto scelto quando è stata eseguita la procedura guidata. Qui verranno modificati i nomi effettivi dei set di impostazioni e questo sarà il modo in cui verranno visualizzati e visualizzati da Windows Media Player.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del codice**](implementing-your-code.md)
</dt> </dl>

 

 




