---
title: Attivazione da sessione a sessione con un moniker di sessione
description: L'attivazione da sessione a sessione (detta anche attivazione tra sessioni) consente a un processo client di avviare (attivare) un processo del server locale in una sessione specificata.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729618"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Attivazione da sessione a sessione con un moniker di sessione

L'attivazione da sessione a sessione (detta anche attivazione tra sessioni) consente a un processo client di avviare (attivare) un processo del server locale in una sessione specificata. Questa funzionalità è disponibile per le applicazioni configurate per l'esecuzione nel contesto di sicurezza dell'utente interattivo, nota anche come modalità di attivazione degli oggetti "RunAs Interactive". Per ulteriori informazioni sui contesti di sicurezza, vedere [il contesto di sicurezza del client](/windows/desktop/SecAuthZ/the-client-security-context).

Distributed COM (DCOM) consente l'attivazione di oggetti in base a ogni sessione usando un moniker di [sessione](session-monikers.md)fornito dal sistema. Altri moniker forniti dal sistema includono [moniker di file](../com/file-monikers.md), moniker di [elementi](../com/item-monikers.md), [moniker compositi](../com/composite-monikers.md)generici, [anti-moniker](../com/anti-monikers.md), [moniker di puntatore](../com/pointer-monikers.md)e [moniker URL](../com/url-monikers.md).

Per poter utilizzare il moniker della sessione, è necessario che l'applicazione DCOM sia impostata per l'esecuzione come utente interattivo. Questa impostazione può essere configurata utilizzando lo strumento di amministrazione Servizi componenti, visualizzando le proprietà dell'applicazione DCOM e selezionando **l'utente interattivo** nella scheda **identità** . Per ulteriori informazioni sui possibili rischi per la sicurezza associati all'impostazione di un'applicazione DCOM per l'esecuzione come utente interattivo in un ambiente di Servizi Desktop remoto, vedere la sezione relativa all'identità dell'applicazione (COM) nella documentazione COM della piattaforma Software Development Kit (SDK).

Se si seleziona un altro tipo di utente per eseguire l'applicazione, il moniker della sessione verrà ignorato dall'applicazione. Il moniker della sessione viene ignorato anche dalle applicazioni server COM+. Per ulteriori informazioni sugli altri metodi per la selezione del tipo di utente per l'esecuzione dell'applicazione, vedere la documentazione COM in Platform SDK.

Per creare un moniker di sessione, è necessario comporre l'ID di sessione della sessione di Servizi Desktop remoto con un moniker della classe che specifica l'ID di classe del server di elaborazione.

**Per creare un moniker di sessione**

1.  Impostare come prefisso il nome visualizzato del moniker della classe con il nome visualizzato del moniker della sessione utilizzando la sintassi seguente:

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    dove *cifre* rappresenta l'ID di sessione della sessione in cui verrà avviato il processo server e dove *ID classe* rappresenta l'ID di classe del server. Si noti che l'ID sessione è un numero in base 10.

    Per i computer che eseguono Windows XP o versioni successive, l'utilizzo della sintassi seguente comporterà l'invio dell'attivazione da parte di COM alla sessione della console fisica attualmente attiva, indipendentemente dal relativo ID di sessione:

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Dopo aver creato il moniker della sessione, è possibile passare il risultato alla funzione [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) o [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .

È possibile usare un moniker di sessione in modo analogo a qualsiasi altro moniker.

Per un esempio di codice che illustra come attivare un processo del server locale in una sessione specificata, vedere [using a Session moniker](using-a-session-moniker.md).

Per ulteriori informazioni sull'attivazione di oggetti, sui moniker forniti dal sistema e sui moniker della classe, vedere la documentazione COM in Platform SDK.

> [!Note]  
> I processi creati tra sessioni hanno un limite superiore per le dimensioni del blocco dell'ambiente. Questo limite è di circa 4 KB, ma può essere maggiore o minore a seconda delle altre informazioni necessarie per creare il processo, ad esempio i nomi file, le directory e i parametri per il nuovo processo.

 

 

 