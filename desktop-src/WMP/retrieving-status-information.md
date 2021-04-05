---
title: Recupero delle informazioni sullo stato
description: Recupero delle informazioni sullo stato
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, recupero dello stato
- archivi online, recupero dello stato
- digitare 2 archivi online, recupero dello stato
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- recupero dello stato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712721"
---
# <a name="retrieving-status-information"></a>Recupero delle informazioni sullo stato

Le informazioni sullo stato vengono aggiornate utilizzando il timer creato nella funzione **init** . Tutti gli Stati vengono aggiornati utilizzando lo stesso timer. Il nome della funzione per l'evento timer è **OnTimer**.

**OnTimer** determina le informazioni da visualizzare in base alla selezione dell'utente, archiviata nella variabile globale denominata g \_ oCurrentDLItem. La funzione verifica prima di tutto se i valori di dimensioni o di avanzamento sono validi e crea una stringa per ogni case.


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



Se un valore è valido, la stringa rappresenta il numero di byte. Se il valore non è valido, ad esempio-1, la stringa fornisce un messaggio per informare l'utente che le informazioni non sono ancora disponibili.

Successivamente, un blocco **Switch** determina se il download per l'elemento selezionato è stato completato o annullato. Se uno dei due casi è true, il valore della dimensione delle variabili o dello stato di avanzamento viene aggiornato di conseguenza.


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



Infine, le informazioni sullo stato vengono visualizzate nell'elemento DIV denominato dlstate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di Download Manager**](using-the-download-manager.md)
</dt> </dl>

 

 




