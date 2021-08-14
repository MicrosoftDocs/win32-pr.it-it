---
description: La virtualizzazione del Registro di sistema è una tecnologia di compatibilità delle applicazioni che consente di reindirizzare le operazioni di scrittura del Registro di sistema con impatto globale a percorsi per utente.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Virtualizzazione del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14d8a82a12be74d3c5f2963e8b4edf47baaa85c4a8299e4ff632284bbac83fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763588"
---
# <a name="registry-virtualization"></a>Virtualizzazione del Registro di sistema

*La virtualizzazione del Registro di* sistema è una tecnologia di compatibilità delle applicazioni che consente di reindirizzare le operazioni di scrittura del Registro di sistema con impatto globale a percorsi per utente. Questo reindirizzamento è trasparente per le applicazioni che leggono o scrivono nel Registro di sistema. È supportato a partire da Windows Vista.

Questa forma di virtualizzazione è una tecnologia provvisoria di compatibilità delle applicazioni. Microsoft intende rimuoverlo dalle versioni future del sistema operativo Windows, perché più applicazioni sono compatibili con Windows Vista e versioni successive di Windows. Pertanto, è importante che l'applicazione non diventi dipendente dal comportamento della virtualizzazione del Registro di sistema nel sistema.

La virtualizzazione è destinata solo a garantire la compatibilità per le applicazioni esistenti. Le applicazioni progettate per Windows Vista e le versioni successive di Windows non devono scrivere in aree di sistema sensibili, né devono basarsi sulla virtualizzazione per risolvere eventuali problemi. Quando si aggiorna il codice esistente per l'esecuzione in Windows Vista e versioni successive di Windows, gli sviluppatori devono assicurarsi che le applicazioni archivino i dati solo in posizioni per utente o in percorsi computer all'interno di %alluserprofile% che usano correttamente un elenco di controllo di accesso (ACL).

Per altre informazioni sulla creazione di applicazioni conformi al controllo dell'account utente, vedere la Guida per gli sviluppatori del controllo [dell'account utente](/previous-versions/dotnet/articles/aa480150(v=msdn.10)).

## <a name="virtualization-overview"></a>Panoramica della virtualizzazione

Prima di Windows Vista, le applicazioni venivano in genere eseguite dagli amministratori. Di conseguenza, le applicazioni potrebbero accedere liberamente ai file di sistema e alle chiavi del Registro di sistema. Se queste applicazioni vengono eseguite da un utente standard, l'esecuzione avrà esito negativo a causa di diritti di accesso insufficienti. Windows Vista e versioni successive di Windows la compatibilità delle applicazioni per queste applicazioni reindirizzando automaticamente queste operazioni. Ad esempio, le operazioni del Registro di sistema all'archivio globale (**HKEY \_ LOCAL MACHINE \_ \\ Software**) vengono reindirizzate a una posizione per utente all'interno del profilo dell'utente nota come archivio virtuale *(* **HKEY USERS Classes \_ \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software**).

La virtualizzazione del Registro di sistema può essere classificata in modo generale nei tipi seguenti:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Aprire Registry Virtualization
</dt> <dd>

Se il chiamante non ha accesso in scrittura a una chiave e tenta di aprire la chiave, la chiave viene aperta con l'accesso massimo consentito per tale chiamante.

Se il flag REG KEY DONT SILENT FAIL è impostato per la \_ \_ \_ chiave, l'operazione ha esito negativo \_ e la chiave non viene aperta. Per altre informazioni, vedere "Controllo della virtualizzazione del Registro di sistema" più avanti in questo argomento.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Scrittura della virtualizzazione del Registro di sistema
</dt> <dd>

Se il chiamante non ha accesso in scrittura a una chiave e tenta di scrivervi un valore o di creare una sottochiave, il valore viene scritto nell'archivio virtuale.

Ad esempio, se un utente limitato tenta di scrivere un valore nella chiave seguente: **HKEY \_ LOCAL MACHINE \_ \\ Software** AppKey1, la virtualizzazione reindirizza l'operazione di scrittura alle classi \\  **HKEY \_ USERS \\ <User SID> \_ \\ VirtualStore Machine \\ \\ Software** \\ *AppKey1*.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Lettura della virtualizzazione del Registro di sistema
</dt> <dd>

Se il chiamante legge da una chiave virtualizzata, il Registro di sistema presenta una visualizzazione unita dei valori virtualizzati (dall'archivio virtuale) e dei valori non virtuali (dall'archivio globale) al chiamante.

Si supponga, ad esempio, **che HKEY \_ LOCAL MACHINE \_ \\ Software** AppKey1 contenga due valori V1 e V2 e che un utente limitato scrive un valore \\  V3 nella chiave. Quando l'utente tenta di leggere i valori da questa chiave, la vista unita include i valori V1 e V2 dall'archivio globale e il valore V3 dall'archivio virtuale.

Si noti che i valori virtuali hanno la precedenza sui valori globali, se presenti. Nell'esempio precedente, anche se l'archivio globale aveva il valore V3 in questa chiave, il valore V3 verrebbe comunque restituito al chiamante dall'archivio virtuale. Se la versione 3 fosse stata eliminata dall'archivio virtuale, la versione 3 verrebbe restituita dall'archivio globale. In altre parole, se la versione 3 deve essere eliminata dalle classi **HKEY \_ USERS \\ <User SID> \_ \\ VirtualStore \\ Machine \\ Software** \\ *AppKey1* ma **HKEY LOCAL MACHINE \_ \_ \\ Software** \\ *AppKey1* ha un valore V3, tale valore verrebbe restituito dall'archivio globale.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Ambito di virtualizzazione del Registro di sistema

La virtualizzazione del Registro di sistema è abilitata solo per gli elementi seguenti:

-   Processi interattivi a 32 bit.
-   Chiavi in **HKEY \_ LOCAL MACHINE \_ \\ Software**.
-   Chiavi in cui un amministratore può scrivere. Se un amministratore non è in grado di scrivere in una chiave, l'applicazione avrebbe avuto esito negativo nelle versioni precedenti di Windows anche se fosse stata eseguita da un amministratore.

La virtualizzazione del Registro di sistema è disabilitata per gli elementi seguenti:

-   Processi a 64 bit.
-   Processi non interattivi, ad esempio i servizi.

    Si noti che l'uso del Registro di sistema come meccanismo di comunicazione tra processi (IPC) tra un servizio (o qualsiasi altro processo per cui non è abilitata la virtualizzazione) e un'applicazione non funzionerà correttamente se la chiave è virtualizzata. Ad esempio, se un servizio antivirus aggiorna i file di firma in base a un valore impostato da un'applicazione, il servizio non aggiornerà mai i file di firma perché il servizio legge dall'archivio globale, ma l'applicazione scrive nell'archivio virtuale.

-   Processi che rappresentano un utente. Se un processo tenta di eseguire un'operazione durante la rappresentazione di un utente, tale operazione non verrà virtualizzata.
-   Processi in modalità kernel, ad esempio i driver.
-   Processi che hanno **richiestoExecutionLevel** specificati nei manifesti.
-   Chiavi e sottochiavi delle **classi software HKEY \_ LOCAL \_ MACHINE, \\ \\** **HKEY LOCAL MACHINE Software \_ Microsoft \_ \\ \\ \\ Windows** e **HKEY LOCAL MACHINE Software \_ Microsoft \_ \\ \\ \\ Windows NT**.

## <a name="controlling-registry-virtualization"></a>Controllo della virtualizzazione del Registro di sistema

Oltre a controllare la virtualizzazione a livello di applicazione usando **requestedExecutionLevel** nel manifesto, un amministratore può abilitare o disabilitare la virtualizzazione in base alla chiave per le chiavi in **HKEY \_ LOCAL MACHINE \_ \\ Software**. A tale scopo, usare l'Reg.exe dell'utilità della riga di comando FLAGS con i flag elencati nella tabella seguente.



| Contrassegno                         | Significato                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ KEY \_ DONT \_ SILENT \_ FAIL | Questo flag disabilita la virtualizzazione del Registro di sistema aperta. Se questo flag è impostato e un'operazione di apertura ha esito negativo su una chiave in cui è abilitata la virtualizzazione, il Registro di sistema non tenta di riaprire la chiave. Se questo flag è deselezionato, il Registro di sistema tenta di riaprire la chiave con l'accesso MAXIMUM \_ ALLOWED anziché con l'accesso richiesto.                                                                   |
| REG \_ KEY \_ DONT \_ VIRTUALIZE   | Questo flag disabilita la virtualizzazione del Registro di sistema di scrittura. Se questo flag è impostato e un'operazione create key o set value ha esito negativo perché il chiamante non dispone di diritti di accesso sufficienti alla chiave padre, il Registro di sistema ha esito negativo. Se questo flag è deselezionato, il Registro di sistema tenta di scrivere la chiave o il valore nell'archivio virtuale. Il chiamante deve disporre del diritto KEY \_ READ sulla chiave padre. |
| \_FLAG DI \_ RICORSIONE DELLA CHIAVE \_ REG      | Se questo flag è impostato, i flag di virtualizzazione del Registro di sistema vengono propagati dalla chiave padre. Se questo flag è deselezionato, i flag di virtualizzazione del Registro di sistema non vengono propagati. La modifica di questo flag influisce solo sulle nuove chiavi discendenti create dopo la modifica del flag. Non imposta o cancella questi flag per le chiavi discendenti esistenti.                                                                  |



 

L'esempio seguente illustra l'uso dell'utilità Reg.exe della riga di comando con l'opzione FLAGS per eseguire query sullo stato dei flag di virtualizzazione per una chiave.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Ogni volta che il controllo viene abilitato in una chiave che viene virtualizzata, viene generato un nuovo evento di controllo della virtualizzazione per indicare che la chiave è in fase di virtualizzazione (oltre ai soliti eventi di controllo). Gli amministratori possono usare queste informazioni per monitorare lo stato della virtualizzazione nei propri sistemi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali controllo dell'account utente](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Informazioni e configurazione del controllo dell'account utente](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Procedure consigliate e linee guida per gli sviluppatori per le applicazioni in un ambiente con privilegi minimi](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
