---
description: Nondeferred azioni personalizzate che chiamano librerie a collegamento dinamico o script possono accedere a un'installazione in esecuzione per eseguire query o modificare gli attributi della sessione di installazione corrente.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967307"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata

Nondeferred azioni personalizzate che chiamano [librerie a collegamento dinamico](dynamic-link-libraries.md) o [script](scripts.md) possono accedere a un'installazione in esecuzione per eseguire query o modificare gli attributi della sessione di installazione corrente. Per ogni processo può esistere un solo oggetto **sessione** e gli script di azione personalizzati non devono tentare di creare un'altra sessione.

Le azioni personalizzate possono aggiungere, modificare o rimuovere solo righe, colonne o tabelle temporanee da un database. Le azioni personalizzate non possono modificare i dati persistenti in un database, ad esempio i dati che fanno parte del database archiviato su disco.

[Librerie a collegamento dinamico](dynamic-link-libraries.md)

Per accedere a un'installazione in esecuzione, le azioni personalizzate che chiamano librerie a collegamento dinamico (DLL) vengono passate un handle del tipo MSIHANDLE per la sessione corrente come unico argomento al punto di ingresso della DLL denominato nella colonna di destinazione della [tabella CustomAction](customaction-table.md). Poiché il programma di installazione fornisce questo handle, l'azione personalizzata non deve chiuderla, ad esempio per ricevere l'handle *hinstall* dal programma di installazione, la funzione azione personalizzata viene dichiarata come indicato di seguito.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Per l'accesso in sola lettura al database corrente, ottenere l'handle di database chiamando [**funzione MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase). Per ulteriori informazioni, vedere [ottenere un handle di database](obtaining-a-database-handle.md).

[Script](scripts.md)

Le azioni personalizzate scritte in VBScript o JScript possono accedere alla sessione di installazione corrente usando l' [**oggetto Session**](session-object.md). Il programma di installazione crea un oggetto **sessione** denominato "Session" che fa riferimento all'installazione corrente. Per l'accesso in sola lettura al database corrente, utilizzare la proprietà [**database**](session-database.md) dell'oggetto **Session** .

Poiché uno script viene eseguito dal contesto dell'oggetto [**sessione**](session-object.md) , non è sempre necessario qualificare completamente le proprietà e i metodi. Nell'esempio seguente, quando si usa VBScript, il riferimento me può sostituire l'oggetto **Session** . ad esempio, le tre righe seguenti sono equivalenti.


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[File eseguibili](executable-files.md)

Non è possibile accedere alla sessione del programma di installazione corrente da azioni personalizzate che chiamano file eseguibili avviati con una riga di comando, ad esempio, il [tipo di azione personalizzata 2](custom-action-type-2.md) e il [tipo di azione personalizzata 18](custom-action-type-18.md).

[Azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md)

Non è possibile accedere alla sessione del programma di installazione corrente o a tutti i dati di proprietà da un'azione personalizzata di esecuzione posticipata. Per altre informazioni, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso a un database o a una sessione dall'interno di un'azione personalizzata](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



