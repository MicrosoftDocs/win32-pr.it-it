---
description: WMI rende disponibili i dati sugli oggetti gestibili da Windows tramite provider WMI.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Invio di dati a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60df0384bd6f512b931870775067d9d9e6d4077d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753682"
---
# <a name="providing-data-to-wmi"></a>Invio di dati a WMI

WMI rende disponibili i dati sugli oggetti gestibili da Windows tramite [*provider*](gloss-p.md)WMI. Un provider recupera i dati da un componente di sistema, ad esempio un processo, o da un'applicazione instrumentata, ad esempio SNMP o IIS, e passa tali dati tramite WMI a un'applicazione di gestione. Ad esempio, quando un'applicazione o uno script richiede l'elaborazione di informazioni utilizzando la classe di [**\_ processo WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) , i dati vengono ottenuti in modo dinamico tramite un provider preinstallato.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Creazione di un modello per un oggetto gestibile](#creating-a-model-for-a-manageable-object)
-   [Implementazione di un modello per un oggetto gestibile](#implementing-a-model-for-a-manageable-object)
-   [Determinazione di un tipo di provider da implementare](#determining-a-provider-type-to-implement)
-   [Determinazione di un modello di hosting (implementazione) per un provider](#determining-a-hosting-implementation-model-for-a-provider)
-   [Implementazione di un provider](#implementing-a-provider)
-   [Registrazione di un provider con WMI e il sistema](#registering-a-provider-with-wmi-and-the-system)
-   [Test di un provider](#testing-a-provider)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>Creazione di un modello per un oggetto gestibile

Prima di sviluppare un provider, creare un modello di dati per rappresentare l'oggetto gestibile da esporre tramite WMI. Si pianificano gli oggetti dati che il provider esporrà. Se ad esempio si prevede di gestire la risoluzione dello schermo dello sfondo del desktop, è necessario decidere come modellare il desktop in un file di [*Managed Object Format (MOF)*](gloss-m.md) .

Per creare un modello utile:

-   Determinare scenari reali e modellare le informazioni che un cliente potrebbe voler leggere e aggiornare (ad esempio, la modifica dell'immagine di sfondo) per ogni oggetto gestibile. Si tratta delle proprietà della classe.
-   Determinare il tipo di azioni che un cliente potrebbe voler eseguire con ogni oggetto gestibile. Questi sono i metodi.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implementazione di un modello per un oggetto gestibile

Per implementare un modello per gli oggetti gestibili, creare un file MOF contenente una classe WMI che rappresenti ogni oggetto. Per ulteriori informazioni sulla creazione di un file MOF per definire classi WMI, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md). La registrazione del provider e delle relative classi viene in genere inclusa nel file MOF, sebbene sia possibile utilizzare l' [API com](com-api-for-wmi.md) per creare classi e metodi. Per ulteriori informazioni, vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md).

> [!Note]  
> Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e viene riavviato, usare l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) nel file [*Managed Object Format (MOF)*](gloss-m.md) .

 

Dopo aver creato il file MOF, compilarlo utilizzando lo strumento [**Mofcomp.exe**](mofcomp.md) . In questo modo viene inviata una notifica all'utente degli errori nel file MOF e viene aggiunta la classe WMI definita nel file MOF al [*repository WMI*](gloss-w.md) , in modo che la classe possa essere utilizzata da un provider.

## <a name="determining-a-provider-type-to-implement"></a>Determinazione di un tipo di provider da implementare

WMI supporta un certo numero di tipi di provider, che determina la natura delle informazioni fornite e le operazioni supportate dai provider.

I tipi di provider sono:

-   [*Provider di istanze*](gloss-i.md)
-   [*Provider di metodi*](gloss-m.md)
-   [*Provider di proprietà*](gloss-p.md)
-   Provider di classi
-   [*Provider di eventi*](gloss-e.md)
-   [*Provider di consumer di eventi*](gloss-e.md)
-   [*Provider di associazioni*](gloss-a.md)

La maggior parte dei provider è costituita da provider di istanze e provider di metodi. Un provider di istanze è il provider più comune e fornisce le istanze di una determinata classe. Un provider di metodi implementa i metodi di una o più classi. Per ulteriori informazioni sui tipi di provider, vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md).

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Determinazione di un modello di hosting (implementazione) per un provider

I provider WMI sono binari implementati come oggetti COM. Questo significa che ogni provider dispone di un file DLL che può essere eseguito all'interno di un processo specifico e di un contesto di sicurezza. Questo è il riferimento a WMI come [*modello di hosting*](gloss-h.md). WMI offre diversi modi per ospitare i provider, ma l'approccio più comune consiste nell'usare il modello di provider associato (in esecuzione nel processo WMI) nel contesto di sicurezza NetworkServiceHost. Un provider WMI può essere classificato come abbinato o [*disaccoppiato*](gloss-d.md).

Il termine provider associato o disaccoppiato determina in quale processo host viene eseguito il provider rispetto al processo WMIPRVSE.EXE fornito da WMI. Una procedura consigliata consiste nel determinare se i dati di gestione esposti dal provider e l'API o l'applicazione su cui si basano sono sempre disponibili nel sistema. Se l'API o l'applicazione su cui si basa il provider è sempre disponibile (in esecuzione nel sistema), il provider deve essere un provider associato. in caso contrario, deve essere un provider disaccoppiato. Per ulteriori informazioni sui modelli di hosting, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

Per ulteriori informazioni sulla creazione di un provider associato, vedere la pagina relativa [alla fornitura di dati a WMI mediante la scrittura di un provider](supplying-data-to-wmi-by-writing-a-provider.md)e per informazioni sull'incorporamento di un provider disaccoppiato in un'applicazione, vedere [incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md).

I provider associati possono essere descritti come in-process (in-process) o out-of-process (out-of-process). Quando un provider associato è un provider in-process, viene eseguito in un processo di hosting WMI WMIPRVSE.EXE condiviso e viene implementato come server in-process COM (. dll). Quando un provider è un provider out-of-process, viene avviato da WMI su richiesta di un client o di un evento, ma viene eseguito come processo separato ed è implementato come file eseguibile (exe).

## <a name="implementing-a-provider"></a>Implementazione di un provider

Un provider può essere implementato nei modi seguenti:

-   Uso della procedura guidata ATL in Visual Studio.

    La procedura guidata ATL genera codice del provider che implementa un provider associato. Quando si utilizza la procedura guidata ATL, è possibile specificare che si desidera creare un modello in fase di esecuzione (con estensione dll) o del provider out-of-process (exe).

-   Definizione di un oggetto COM che contenga il provider.

    Il codice del provider è scritto in C++. Per ulteriori informazioni, vedere [la pagina relativa alla fornitura di dati a WMI mediante la scrittura di un provider](supplying-data-to-wmi-by-writing-a-provider.md).

-   Utilizzare le classi nello spazio dei nomi [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) nel .NET Framework per creare un provider utilizzando codice gestito. Lo spazio dei nomi **System. Management. Instrumentation** non è più supportato.

    Questo processo crea un provider disaccoppiato.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Registrazione di un provider con WMI e il sistema

Prima di utilizzare il provider da un consumer, è importante registrarlo nel sistema WMI e nel sottosistema COM di Windows.

Un file MOF può contenere più tipi di provider per le stesse classi. Lo stesso nome del provider viene registrato come, ad esempio, un'istanza o un provider di metodi. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).

## <a name="testing-a-provider"></a>Test di un provider

Quando il codice del provider viene registrato, è importante testare correttamente il provider utilizzando il provider di consumer diversi, ad esempio script, codice gestito .NET e consumer C++.

Per testare il provider, eseguire le attività seguenti:

-   Verificare che il provider sia stato caricato correttamente tenendo traccia delle notifiche degli eventi di [**MSFT \_ provider WMI \_ OperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) . Questi eventi forniranno informazioni sugli errori di caricamento del provider. Altre classi di risoluzione dei problemi che possono essere utili sono [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) e [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace). Per ulteriori informazioni sulla risoluzione dei problemi relativi ai provider, vedere [debug](debugging-providers.md) di provider e [classi di risoluzione dei problemi e di configurazione del provider](provider-configuration-and-troubleshooting-classes.md).
-   Se il provider è un'istanza o un provider di metodi, assicurarsi di testare ogni funzionalità del provider una alla volta per evitare confusione nel seguito della logica del codice.
-   Per un provider di istanze, creare un'applicazione client o uno script che richiama ogni interfaccia del provider (enumerazione, Get, Put ed Delete). Anche se non è previsto che il provider implementi alcun elemento, deve restituire un messaggio "non supportato". È possibile trovare i valori restituiti già definiti nei [codici restituiti WMI](wmi-return-codes.md).
-   Per assicurarsi che il contesto di sicurezza desiderato funzioni come previsto, richiamare le operazioni supportate dal provider da un contesto di sicurezza non amministratore. Il provider deve supportare la rappresentazione. Se un utente privo delle credenziali di sicurezza corrette tenta di aggiornare i dati o di eseguire un'operazione che esegue un metodo, il provider deve negare l'accesso con il messaggio di errore appropriato.
-   Per ulteriori informazioni sulla sicurezza del provider, vedere la pagina relativa alla protezione [del provider](securing-your-provider.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hosting e sicurezza del provider](provider-hosting-and-security.md)
</dt> <dt>

[Fornire dati a WMI scrivendo un provider](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Registrazione di un provider](registering-a-provider.md)
</dt> <dt>

[Risoluzione dei problemi relativi alle applicazioni client WMI](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Sicurezza del provider](securing-your-provider.md)
</dt> <dt>

[Ottenere e fornire dati in una piattaforma a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
