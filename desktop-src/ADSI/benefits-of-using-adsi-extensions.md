---
title: Vantaggi dell'utilizzo delle estensioni ADSI
description: Il modo in cui vengono implementati i metodi di estensione dipende dal writer di estensione.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27e80e6c095fcc02ca02c57b0987d1e6ed410ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044075"
---
# <a name="benefits-of-using-adsi-extensions"></a>Vantaggi dell'utilizzo delle estensioni ADSI

Il modo in cui vengono implementati i metodi di estensione dipende dal writer di estensione. Un writer di estensione può persino implementare un metodo completamente al di fuori dell'ambito della directory. Uno sviluppatore di software di backup e ripristino prevede ad esempio l'estensione di un oggetto denominato **computer**. Lo sviluppatore deve creare due metodi: **backup** e **ripristino**. Questi metodi operano in modalità remota sul computer fisico a cui punta l'oggetto **computer** nella directory. Agendo come un'estensione, il componente accede all'infrastruttura ADSI e viene visualizzato dai client ADSI come parte integrante dell'oggetto.

Negli scenari seguenti vengono descritte le situazioni in cui è vantaggioso creare un'estensione per ADSI:

-   Creare un'estensione per integrare un componente con l'oggetto directory. Poiché nella directory è presente un oggetto **utente** , è possibile che uno sviluppatore HR voglia creare un'estensione ADSI che compila altri dati nella directory quando viene creato un **utente** .
-   Creare un'estensione se un componente richiede una ricerca nella directory. Un componente può richiedere una directory come punto di partenza per una ricerca. Ad esempio, quando si crea una nuova applicazione. Un oggetto applicazione, **ToolApp**, può essere pubblicato nella directory. L'applicazione può supportare le notifiche di stato in una raccolta di server di posta. Si decide di rendere questa applicazione un'estensione ADSI.

    A questo punto, un utente può cercare tutte le istanze di **ToolApp** nella directory. Per ogni oggetto restituito, l'utente può eseguire una chiamata a **NotifyNow ()**. Un'applicazione o un'estensione può ottenere più dati oggetto correnti nella directory e inviare una notifica in modo asincrono a ogni server.

-   Creare un'estensione come giunzione tra gli spazi dei nomi e i modelli di programmazione. Un ISV, ad esempio, inventa un nuovo modello a oggetti per i servizi di stampa. L'oggetto **PrintQueue** è già definito nella directory. Il ISV può creare un'estensione ADSI e associarla all'oggetto **PrintQueue** . Gli utenti ADSI possono eseguire l'associazione a un oggetto **PrintQueue** e iniziare a utilizzare il modello a oggetti per l'ISV. Dal punto di vista del client ADSI, questo punto di giunzione è trasparente.
-   Creare un'estensione per semplificare le attività. Molte attività nella directory possono essere eseguite eseguendo la ricerca e l'impostazione di più attributi in un oggetto o più oggetti. Creando una singola funzione per modificare più attributi, semplifica lo sviluppo di applicazioni e writer di script.

Per i client ADSI, le estensioni arricchiscono l'ambiente di programmazione ADSI in diversi modi:

-   Gli sviluppatori che creano client ADSI non devono apprendere un nuovo modello di programmazione. Le estensioni fanno parte di ADSI. Utilizzeranno lo stesso paradigma per la ricerca, la manipolazione dei dati e la protezione degli oggetti.
-   Gli amministratori possono gestire applicazioni correlate abilitate alla directory usando le estensioni.
-   I consumer di estensione possono visualizzare un oggetto e un'estensione ADSI come un unico oggetto integrato.
-   I componenti esistenti possono essere integrati con ADSI, che consente alle estensioni di sfruttare gli investimenti esistenti e creare sinergie tra i componenti.

Le estensioni ADSI sono state progettate con gli obiettivi seguenti:

-   Facile da implementare. Con le attuali tecnologie Microsoft, Microsoft Visual C++ sistema di sviluppo e la Active Template Library, è possibile creare rapidamente un'estensione.
-   I client visualizzano un IDispatch. Dal punto di vista dei writer di script e di automazione, le proprietà e i metodi di estensione vengono combinati in modo trasparente in un unico oggetto ADSI.
-   Indipendenti. I writer di estensione possono estendere in modo indipendente ADSI senza conoscere prima le estensioni esistenti.

Si consideri questo scenario: uno sviluppatore aziendale o un ISV deve sviluppare un programma di backup. Questa applicazione di backup consente a un amministratore di eseguire il backup di tutti i computer in un'unità organizzativa. Con un'estensione ADSI, è possibile usare lo script seguente.


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



**LastBackUp** è una proprietà e **BackUpNow** è un metodo fornito dal writer di estensione. Il codice mostra i vantaggi sia per gli utenti che per i provider di estensioni. Il writer di estensione non è in grado di creare un nuovo modo di filtrare, cercare e accedere alla directory. Il consumer dell'estensione non deve riapprendere un nuovo paradigma di programmazione. I nuovi metodi e proprietà forniti dal writer di estensione vengono visualizzati come parte di ADSI.

 

 




