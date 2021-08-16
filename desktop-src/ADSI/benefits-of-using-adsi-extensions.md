---
title: Vantaggi dell'uso delle estensioni ADSI
description: La modalità di implementazione dei metodi di estensione dipende dal writer di estensione.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a680e1eefbc05dac84b3420bee23287eda2bd02325274532109544b04ff73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018144"
---
# <a name="benefits-of-using-adsi-extensions"></a>Vantaggi dell'uso delle estensioni ADSI

La modalità di implementazione dei metodi di estensione dipende dal writer di estensione. Un writer di estensione può anche implementare un metodo completamente esterno all'ambito della directory. Ad esempio, uno sviluppatore di piani software di backup e ripristino per estendere un oggetto denominato **computer**. Lo sviluppatore deve creare due metodi: **BackUp** e **Restore.** Questi metodi operano in remoto sul computer fisico a cui punta **l'oggetto computer** nella directory. Fungendo da estensione, il componente accede all'infrastruttura ADSI e viene visualizzato dai client ADSI come parte integrante dell'oggetto.

Gli scenari seguenti descrivono situazioni in cui la creazione di un'estensione ad ADSI sarebbe vantaggiosa:

-   Creare un'estensione per integrare un componente con l'oggetto directory. Poiché nella directory **è** presente un oggetto utente, uno sviluppatore di risorse umane potrebbe voler creare un'estensione ADSI che popola altri dati nella directory quando viene creato **un** utente.
-   Creare un'estensione se un componente richiede una ricerca nella directory. Un componente può richiedere una directory come punto di partenza per una ricerca. Ad esempio, quando si crea una nuova applicazione. Un oggetto applicazione, **ToolApp,** può essere pubblicato nella directory . L'applicazione può supportare le notifiche di stato in una raccolta di server di posta elettronica. Si decide di rendere questa applicazione un'estensione ADSI.

    A questo punto, un utente può cercare tutte le istanze **di ToolApp** nella directory. Per ogni oggetto restituito, l'utente può eseguire una chiamata a **NotifyNow().** Un'applicazione o un'estensione può ottenere dati oggetto più correnti nella directory e inviare una notifica a ogni server in modo asincrono.

-   Creare un'estensione come giunzione tra spazi dei nomi e modelli di programmazione. Ad esempio, un ISV inventa un nuovo modello a oggetti per i servizi di stampa. **L'oggetto printQueue** è già definito nella directory . L'ISV può creare un'estensione ADSI e associarla **all'oggetto printQueue.** Gli utenti ADSI possono eseguire l'associazione a **un oggetto printQueue** e iniziare a usare il modello a oggetti per l'ISV. Dal punto di vista del client ADSI, questo punto di giunzione è trasparente.
-   Creare un'estensione per semplificare le attività. Molte attività nella directory possono essere eseguite eseguendo ricerche e impostando più attributi in uno o più oggetti. La creazione di una singola funzione per modificare più attributi semplifica lo sviluppo per writer di applicazioni e script.

Per i client ADSI, le estensioni arricchiscono l'ambiente di programmazione ADSI in diversi modi:

-   Gli sviluppatori che creano client ADSI non devono apprendere un nuovo modello di programmazione. Le estensioni fanno parte di ADSI. Usano lo stesso paradigma per la ricerca, la manipolazione dei dati e la protezione degli oggetti.
-   Gli amministratori possono gestire le applicazioni abilitate per la directory correlate usando le estensioni.
-   I consumer di estensioni possono visualizzare un oggetto ADSI e un'estensione come un unico oggetto integrato.
-   I componenti esistenti possono essere integrati con ADSI, che consente alle estensioni di sfruttare gli investimenti esistenti e creare una combinazione di componenti.

Le estensioni ADSI sono state progettate con gli obiettivi seguenti:

-   Facile da implementare. Con le tecnologie Microsoft esistenti, il Microsoft Visual C++ di sviluppo e il Active Template Library, è possibile creare rapidamente un'estensione.
-   I client visualizzano un IDispatch. Dal punto di vista dei writer di script e di automazione, i metodi e le proprietà di estensione vengono uniti in modo trasparente in un unico oggetto ADSI.
-   Indipendente. I writer di estensioni possono estendere in modo indipendente ADSI senza conoscere in precedenza le estensioni esistenti.

Si consideri questo scenario: uno sviluppatore aziendale o un ISV deve sviluppare un programma di backup. Questa applicazione di backup consente a un amministratore di eseguire il backup di tutti i computer in un'unità organizzativa. Con un'estensione ADSI, è possibile eseguire lo script seguente.


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



**LastBackUp** è una proprietà e **BackUpNow** è un metodo fornito dal writer di estensione. Il codice illustra i vantaggi sia per i consumer di estensioni che per i provider. Il writer di estensioni non deve creare un nuovo modo per filtrare, cercare e accedere alla directory. Il consumer di estensioni non deve rilevare un nuovo paradigma di programmazione. I nuovi metodi e proprietà forniti dal writer di estensione vengono visualizzati come parte di ADSI.

 

 




