---
description: Le azioni personalizzate non gestite che chiamano librerie o script a collegamento dinamico possono accedere a un'installazione in esecuzione per eseguire query o modificare gli attributi della sessione di installazione corrente.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Accesso alla sessione del programma di installazione corrente dall'interno di un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ee3214b8f8664b57f5216b28a7f5d5269d76049fe5c4dd24f7ab8d130d89a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640190"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Accesso alla sessione del programma di installazione corrente dall'interno di un'azione personalizzata

Le azioni personalizzate non gestite [](dynamic-link-libraries.md) che chiamano [](scripts.md) librerie o script a collegamento dinamico possono accedere a un'installazione in esecuzione per eseguire query o modificare gli attributi della sessione di installazione corrente. Per ogni **processo può** esistere un solo oggetto Session e gli script delle azioni personalizzate non devono tentare di creare un'altra sessione.

Le azioni personalizzate possono solo aggiungere, modificare o rimuovere righe, colonne o tabelle temporanee da un database. Le azioni personalizzate non possono modificare i dati persistenti in un database, ad esempio i dati che fanno parte del database archiviato su disco.

[Librerie a collegamento dinamico](dynamic-link-libraries.md)

Per accedere a un'installazione in esecuzione, alle azioni personalizzate che chiamano librerie a collegamento dinamico (DLL) viene passato un handle del tipo MSIHANDLE per la sessione corrente come unico argomento per il punto di ingresso DLL denominato nella colonna Target della [tabella CustomAction](customaction-table.md). Poiché il programma di installazione fornisce questo handle, l'azione personalizzata non deve chiuderla, ad esempio per ricevere l'handle *hInstall* dal programma di installazione, la funzione di azione personalizzata viene dichiarata come segue.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Per l'accesso in sola lettura al database corrente, ottenere l'handle del database chiamando [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase). Per altre informazioni, vedere [Recupero di un handle di database](obtaining-a-database-handle.md).

[Script](scripts.md)

Le azioni personalizzate scritte in VBScript o JScript possono accedere alla sessione di installazione corrente usando [**l'oggetto sessione**](session-object.md). Il programma di installazione crea **un oggetto Session** denominato "Session" che fa riferimento all'installazione corrente. Per l'accesso in sola lettura al database corrente, usare la [**proprietà Database**](session-database.md) **dell'oggetto** Session.

Poiché uno script viene eseguito dal contesto [**dell'oggetto Session,**](session-object.md) non è sempre necessario qualificare completamente le proprietà e i metodi. Nell'esempio seguente, quando si usa VBScript, il riferimento Me può sostituire l'oggetto **Session,** ad esempio le tre righe seguenti sono equivalenti.


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

Non è possibile accedere alla sessione del programma di installazione corrente da azioni personalizzate che chiamano file eseguibili avviati con una riga di comando, ad esempio Custom [Action Type 2](custom-action-type-2.md) e [Custom Action Type 18.](custom-action-type-18.md)

[Azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md)

Non è possibile accedere alla sessione corrente del programma di installazione o a tutti i dati delle proprietà da un'azione personalizzata di esecuzione posticipata. Per altre informazioni, vedere [Recupero di informazioni di contesto per azioni personalizzate di esecuzione posticipata.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso a un database o a una sessione dall'interno di un'azione personalizzata](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



