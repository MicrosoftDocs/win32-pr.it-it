---
title: Attivazione da sessione a sessione con un moniker di sessione
description: L'attivazione da sessione a sessione (detta anche attivazione tra sessioni) consente a un processo client di avviare (attivare) un processo server locale in una sessione specificata.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213627facdd2dee9e4ba7cc698d2be5455424b4394d295448a07aeb52788dd42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988131"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Attivazione da sessione a sessione con un moniker di sessione

L'attivazione da sessione a sessione (detta anche attivazione tra sessioni) consente a un processo client di avviare (attivare) un processo server locale in una sessione specificata. Questa funzionalità è disponibile per le applicazioni configurate per l'esecuzione nel contesto di sicurezza dell'utente interattivo, nota anche come modalità di attivazione dell'oggetto "RunAs Interactive User". Per altre informazioni sui contesti di sicurezza, vedere [Contesto di sicurezza del client.](/windows/desktop/SecAuthZ/the-client-security-context)

Distributed COM (DCOM) consente l'attivazione di oggetti per sessione tramite un [moniker](session-monikers.md)di sessione fornito dal sistema. Altri moniker forniti dal sistema includono moniker di [file,](../com/file-monikers.md)moniker di [elementi,](../com/item-monikers.md)moniker compositi [generici,](../com/composite-monikers.md) [anti-moniker,](../com/anti-monikers.md)moniker puntatore e moniker [URL.](../com/url-monikers.md) [](../com/pointer-monikers.md)

Per poter usare il moniker di sessione, l'applicazione DCOM deve essere impostata per l'esecuzione come utente interattivo. Questa impostazione può essere impostata tramite lo strumento amministrativo Servizi componenti, visualizzando le proprietà dell'applicazione DCOM e selezionando **L'utente** interattivo nella **scheda** Identità. Per altre informazioni sui possibili rischi per la sicurezza associati all'impostazione di un'applicazione DCOM da eseguire come utente interattivo in un ambiente Servizi Desktop remoto, vedere la sezione "Identità dell'applicazione (COM)" della documentazione COM in Platform Software Development Kit (SDK).

Se si seleziona un altro tipo di utente per eseguire l'applicazione, il moniker di sessione verrà ignorato dall'applicazione. Il moniker di sessione viene ignorato anche dalle applicazioni server COM+. Per altre informazioni su altri metodi per la selezione del tipo di utente per eseguire l'applicazione, vedere la documentazione COM in Platform SDK.

Per creare un moniker di sessione, è necessario comporre l'ID sessione della sessione Servizi Desktop remoto con un moniker di classe che specifica l'ID di classe del server di elaborazione.

**Per creare un moniker di sessione**

1.  Aggiungere al nome visualizzato del moniker della classe il nome visualizzato del moniker di sessione usando la sintassi seguente:

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    dove *digits* rappresenta l'ID sessione della sessione in cui verrà avviato il processo server e dove *class id* rappresenta l'ID classe del server. Si noti che l'ID sessione è un numero in base 10.

    Per i computer che eseguono Windows XP o versioni successive, l'uso della sintassi seguente comporterà l'invio com dell'attivazione alla sessione della console fisica attualmente attiva, indipendentemente dal relativo ID di sessione:

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Dopo aver creato il moniker di sessione, è possibile passare il risultato alla funzione [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) o [MkParseDisplayNameEx.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85))

È possibile usare un moniker di sessione nello stesso modo in cui si userebbe qualsiasi altro moniker.

Per un esempio di codice che illustra come attivare un processo server locale in una sessione specificata, vedere [Uso di un moniker di sessione](using-a-session-moniker.md).

Per altre informazioni sull'attivazione degli oggetti, sui moniker forniti dal sistema e sui moniker di classe, vedere la documentazione COM in Platform SDK.

> [!Note]  
> I processi creati tra le sessioni hanno un limite massimo per le dimensioni del blocco di ambiente. Questo limite è di circa 4 KB, ma può essere maggiore o minore a seconda delle altre informazioni necessarie per creare il processo, ad esempio nomi di file, directory e parametri per il nuovo processo.

 

 

 