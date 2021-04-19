---
description: La virtualizzazione del registro di sistema è una tecnologia di compatibilità delle applicazioni che consente di reindirizzare le operazioni di scrittura del registro di sistema a posizioni per utente.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Virtualizzazione del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642bda46b43fc0b4f7efa60cfcd9e2178643811f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319888"
---
# <a name="registry-virtualization"></a>Virtualizzazione del registro di sistema

La *virtualizzazione del registro di sistema* è una tecnologia di compatibilità delle applicazioni che consente di reindirizzare le operazioni di scrittura del registro di sistema a posizioni per utente. Questo reindirizzamento è trasparente per le applicazioni che leggono o scrivono nel registro di sistema. È supportato a partire da Windows Vista.

Questa forma di virtualizzazione è una tecnologia provvisoria per la compatibilità delle applicazioni. Microsoft intende rimuoverlo dalle versioni future del sistema operativo Windows, in quanto le altre applicazioni vengono rese compatibili con Windows Vista e versioni successive di Windows. Pertanto, è importante che l'applicazione non diventi dipendente dal comportamento della virtualizzazione del registro di sistema nel sistema.

La virtualizzazione è destinata solo a garantire la compatibilità per le applicazioni esistenti. Le applicazioni progettate per Windows Vista e le versioni successive di Windows non devono scrivere in aree di sistema sensibili, né devono basarsi sulla virtualizzazione per risolvere eventuali problemi. Quando si aggiorna il codice esistente per l'esecuzione in Windows Vista e nelle versioni successive di Windows, gli sviluppatori devono assicurarsi che le applicazioni memorizzino solo i dati in percorsi per utente o in posizioni del computer all'interno di% ALLUSERPROFILE% che usino correttamente un elenco di controllo di accesso (ACL).

Per ulteriori informazioni sulla compilazione di applicazioni conformi a UAC, vedere la [Guida per sviluppatori UAC](/previous-versions/dotnet/articles/aa480150(v=msdn.10)).

## <a name="virtualization-overview"></a>Panoramica della virtualizzazione

Prima di Windows Vista, le applicazioni venivano generalmente eseguite dagli amministratori. Di conseguenza, le applicazioni possono accedere liberamente ai file di sistema e alle chiavi del registro di sistema. Se queste applicazioni venivano eseguite da un utente standard, avrebbero esito negativo a causa di diritti di accesso insufficienti. Windows Vista e le versioni successive di Windows migliorano la compatibilità delle applicazioni per queste applicazioni tramite il reindirizzamento automatico di tali operazioni. Ad esempio, le operazioni del registro di sistema per l'archivio globale (**\_ \_ \\ software del computer locale HKEY**) vengono reindirizzate a una posizione per utente all'interno del profilo dell'utente noto come *archivio virtuale* (**HKEY \_ Users \\ <User SID> \_ Classes \\ VirtualStore \\ Machine \\ software**).

La virtualizzazione del registro di sistema può essere ampiamente classificata nei seguenti tipi:

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Apri la virtualizzazione del registro di sistema
</dt> <dd>

Se il chiamante non dispone dell'accesso in scrittura a una chiave e tenta di aprire la chiave, la chiave viene aperta con l'accesso massimo consentito per quel chiamante.

Se \_ \_ \_ \_ per la chiave è impostato il flag reg key dont Silent Fail, l'operazione ha esito negativo e la chiave non è aperta. Per ulteriori informazioni, vedere "controllo della virtualizzazione del registro di sistema" più avanti in questo argomento.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Scrivi la virtualizzazione del registro di sistema
</dt> <dd>

Se il chiamante non dispone dell'accesso in scrittura a una chiave e tenta di scrivervi un valore o di creare una sottochiave, il valore viene scritto nell'archivio virtuale.

Se, ad esempio, un utente con limitazioni tenta di scrivere un valore nella chiave seguente **: \_ HKEY \_ computer locale \\ software** \\ *AppKey1*, la virtualizzazione reindirizza l'operazione di scrittura a **HKEY \_ utenti \\ <User SID> \_ classi \\ VirtualStore \\ computer \\ software** \\ *AppKey1*.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Leggi la virtualizzazione del registro
</dt> <dd>

Se il chiamante legge da una chiave virtualizzata, il registro di sistema presenta una visualizzazione unita dei valori virtualizzati (dall'archivio virtuale) e dei valori non virtuali (dall'archivio globale) al chiamante.

Si supponga, ad esempio, che **HKEY \_ Local \_ Machine \\ software** \\ *AppKey1* contenga due valori V1 e V2 e che un utente con limitazioni scriva un valore V3 nella chiave. Quando l'utente tenta di leggere i valori da questa chiave, la visualizzazione unita include i valori V1 e V2 dall'archivio globale e il valore V3 dall'archivio virtuale.

Si noti che i valori virtuali hanno la precedenza sui valori globali, se presenti. Nell'esempio precedente, anche se l'archivio globale presentava il valore V3 sotto questa chiave, il valore V3 verrebbe comunque restituito al chiamante dall'archivio virtuale. Se V3 venisse eliminato dall'archivio virtuale, l'archivio globale restituirebbe V3. In altre parole, se V3 venisse eliminato dalle **\_ classi HKEY Users \\ <User SID> \_ \\ VirtualStore \\ Machine \\ software** \\ *AppKey1* ma **HKEY \_ Local \_ Machine \\ software** \\ *AppKey1* aveva un valore V3, tale valore verrebbe restituito dall'archivio globale.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Ambito di virtualizzazione del registro di sistema

La virtualizzazione del registro di sistema è abilitata solo per gli elementi seguenti:

-   processi interattivi a 32 bit.
-   Chiavi nel **\_ software del \_ computer \\ locale HKEY**.
-   Chiavi in cui un amministratore può scrivere. Se un amministratore non è in grado di scrivere su una chiave, l'applicazione potrebbe non riuscire nelle versioni precedenti di Windows, anche se è stata eseguita da un amministratore.

La virtualizzazione del registro di sistema è disabilitata per quanto segue:

-   processi a 64 bit.
-   Processi non interattivi, ad esempio i servizi.

    Si noti che l'uso del registro di sistema come meccanismo di comunicazione interprocesso (IPC) tra un servizio (o qualsiasi altro processo che non dispone della virtualizzazione abilitata) e che un'applicazione non funzionerà correttamente se la chiave è virtualizzata. Ad esempio, se un servizio antivirus aggiorna i file della firma in base a un valore impostato da un'applicazione, il servizio non aggiornerà mai i file della firma perché il servizio legge dall'archivio globale, ma l'applicazione scrive nell'archivio virtuale.

-   Processi che rappresentano un utente. Se un processo tenta di eseguire un'operazione durante la rappresentazione di un utente, tale operazione non verrà virtualizzata.
-   Processi in modalità kernel quali i driver.
-   Processi con **requestedExecutionLevel** specificati nei rispettivi manifesti.
-   Chiavi e sottochiavi delle **\_ \_ \\ \\ classi software del computer locale HKEY**, **\_ software del computer locale HKEY \_ \\ \\ Microsoft \\ Windows** e **HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Windows NT**.

## <a name="controlling-registry-virtualization"></a>Controllo della virtualizzazione del registro di sistema

Oltre a controllare la virtualizzazione a livello di applicazione usando **requestedExecutionLevel** nel manifesto, un amministratore può abilitare o disabilitare la virtualizzazione per chiavi in base al **\_ \_ \\ software del computer locale HKEY**. A tale scopo, usare l'opzione Reg.exe flag dell'utilità della riga di comando con i flag elencati nella tabella seguente.



| Contrassegno                         | Significato                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_chiave reg \_ \_ \_ non riuscita | Questo flag Disabilita la virtualizzazione aperta del registro di sistema. Se questo flag è impostato e un'operazione di apertura non riesce su una chiave abilitata per la virtualizzazione, il registro di sistema non tenta di riaprire la chiave. Se questo flag è chiaro, il registro di sistema tenta di riaprire la chiave con l' \_ accesso massimo consentito anziché l'accesso richiesto.                                                                   |
| \_chiave reg \_ dont \_ virtualizzare   | Questo flag Disabilita la virtualizzazione del registro di sistema per la scrittura. Se questo flag è impostato e l'operazione Create Key o set value ha esito negativo perché il chiamante non dispone di diritti di accesso sufficienti per la chiave padre, l'operazione non riesce. Se questo flag è chiaro, il registro di sistema tenta di scrivere la chiave o il valore nell'archivio virtuale. Il chiamante deve avere la chiave \_ Read right sulla chiave padre. |
| \_flag di \_ rimaledizione della chiave reg \_      | Se questo flag è impostato, i flag di virtualizzazione del registro di sistema vengono propagati dalla chiave padre. Se questo flag è chiaro, i flag di virtualizzazione del registro di sistema non vengono propagati. La modifica di questo flag influiscono solo sulle nuove chiavi discendenti create dopo la modifica del flag. Non imposta o deseleziona questi flag per le chiavi discendenti esistenti.                                                                  |



 

Nell'esempio seguente viene illustrato l'utilizzo dell'utilità della riga di comando Reg.exe con l'opzione FLAGs per eseguire una query sullo stato dei flag di virtualizzazione per una chiave.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Ogni volta che il controllo è abilitato su una chiave virtualizzata, viene generato un nuovo evento di controllo della virtualizzazione per indicare che la chiave è stata virtualizzata (oltre ai normali eventi di controllo). Gli amministratori possono utilizzare queste informazioni per monitorare lo stato della virtualizzazione nei propri sistemi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con controllo dell'account utente](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Informazioni e configurazione del controllo dell'account utente](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Procedure consigliate e linee guida per gli sviluppatori per le applicazioni in un ambiente con privilegi minimi](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
