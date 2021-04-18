---
description: I file di log WMI non sono più supportati.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Registrazione dell'attività WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314598"
---
# <a name="logging-wmi-activity"></a>Registrazione dell'attività WMI

I file di log WMI non sono più supportati. A partire da Windows Vista, WMI utilizza [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) ed eventi disponibili tramite l'interfaccia utente **Visualizzatore eventi** o lo strumento da riga di comando wevtutil. Per ulteriori informazioni, vedere il provider ETW e la documentazione della riga di comando [programma](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .

Le sezioni seguenti sono illustrate in questo argomento:

-   [File di log WMI precedenti a Windows Vista](#wmi-log-files-before-windows-vista)
-   [Registrazione delle attività per i componenti di base di WMI prima di Windows Vista](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [Registrazione di attività per i componenti del provider WMI precedenti a Windows Vista](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [Argomenti correlati](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a>File di log WMI precedenti a Windows Vista

I file di log creati da WMI e da diversi provider registrano: eventi, dati di traccia o di diagnostica, errori e varie attività. Solo gli amministratori hanno accesso in lettura alla cartella dei log WMI presente nei log di% windir% \\ system32 \\ WBEM \\ .

Solo i componenti di base WMI o i provider WMI scrivono nei file di log. È possibile leggere o visualizzare solo i dati presenti nei log per scopi diagnostici. È possibile creare e archiviare i propri file di log nella directory dei log WMI.

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a>Registrazione delle attività per i componenti di base di WMI prima di Windows Vista

Questi file non contengono un formato coerente adatto per la lettura a livello di codice. Per ulteriori informazioni su log specifici, vedere [file di log WMI](wmi-log-files.md).

Quando vengono impostate le chiavi del registro di sistema seguenti, le attività di registrazione per i componenti di base di WMI:

-   Livello di registrazione

    Le modifiche al valore del registro di sistema a livello di registrazione diventano effettive immediatamente. Non è necessario riavviare il servizio WMI.

    **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging** = 2

    Nell'elenco seguente sono elencati i livelli di registrazione che possono essere definiti nel registro di sistema.

    

    | Livello di registrazione | Descrizione               |
    |---------------|---------------------------|
    | 0             | Nessuna registrazione                |
    | 1             | Registra solo gli errori           |
    | 2             | Registrazione dettagliata (impostazione predefinita) |

    

     

-   Posizione dei file di log

    Per rendere effettive le modifiche al percorso del file di log, riavviare il servizio WMI.

    **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging directory** =% windir% \\ system32 \\ WBEM \\ logs

-   Dimensioni massime del file di log, in byte

    **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **dimensioni massime file di log** = 65536

È possibile modificare questi valori della chiave del registro di sistema tramite l'editor del registro di sistema o tramite lo snap-in WMI per Microsoft Management Console.

**Per impostare il livello di registrazione per WMI prima di Windows Vista**

1.  Fare clic sul pulsante **Start** e quindi scegliere **Esegui**.
2.  Digitare **wmimgmt. msc**
3.  Nel menu **Azione** fare clic su **Proprietà**.
4.  Nella scheda **registrazione** impostare il livello di registrazione su **disabilitato**, **abilitato** o **dettagliato**.
5.  In **percorso:** Digitare il percorso della cartella del file di log e in **dimensioni massime (byte):**, impostare la dimensione massima, in byte, del file di log.

Per ulteriori informazioni sull'impostazione delle proprietà dei file di log, vedere la Guida in linea per l'applicazione di controllo WMI.

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a>Registrazione di attività per i componenti del provider WMI precedenti a Windows Vista

Quando è abilitata la registrazione per i componenti di base di WMI, la registrazione viene abilitata anche per qualsiasi provider con funzionalità di registrazione.

Nell'elenco seguente sono elencati i valori necessari.

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>**File**
</dt> <dd>

Percorso completo e nome file del file di log. Il valore predefinito è% windir% \\ system32 \\ \\ log WBEM. Il **tipo** denominato value deve essere impostato su = file affinché questo valore denominato venga usato.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Livello**
</dt> <dd>

Maschera logica a 32 bit che definisce il tipo di output di debug generato dal provider. Questo valore dipende dal provider. Il valore predefinito è 0 (zero).

</dd> <dt>

<span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**
</dt> <dd>

Dimensioni massime del file di log in byte. Il valore intero deve essere compreso tra 1024 e 2 ^ 32-1. Quando le dimensioni del file superano questo valore, il file viene rinominato in **~ filename** e viene creato un nuovo file di log vuoto. Lo spazio su disco necessario per il file di log è il doppio del valore di **MaxFileSize**. Il valore predefinito è 65.535.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**
</dt> <dd>

Può essere impostato su = file o = debugger. Se impostato su = file, le informazioni di traccia vengono scritte nel file di log specificato nel **file** denominato value. Il valore predefinito è = file.

</dd> </dl>

Ad esempio, per registrare la query e ottenere le chiamate di istanza dal provider di visualizzazione, usare i valori della chiave del registro di sistema seguenti. Il log verrà inserito nella cartella log e sarà la dimensione predefinita del file.

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **file** = C: \\ Windows \\ system32 \\ WBEM \\ logs \\ ViewProvider. log

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **registrazione** \\  \\ **livello** ViewProvider = 2

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **MaxFileSize** = 65535

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **Type** = file

> [!Note]  
> Per i provider con funzionalità di registrazione, è necessario scrivere le chiavi e i valori del registro di sistema necessari per abilitare la registrazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

[File di log WMI](wmi-log-files.md)
</dt> <dt>

[Classi di risoluzione dei problemi WMI](wmi-troubleshooting-classes.md)
</dt> <dt>

[Traccia dell'attività WMI](tracing-wmi-activity.md)
</dt> </dl>

 

 
