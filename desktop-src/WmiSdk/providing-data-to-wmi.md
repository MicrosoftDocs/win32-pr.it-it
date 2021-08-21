---
description: WMI rende disponibili i dati Windows oggetti gestibili tramite i provider WMI.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Fornire dati a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22fbff46959c001f589587f21b8b2b50ab5c5187d387338f407bf45e3e1a29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316575"
---
# <a name="providing-data-to-wmi"></a>Fornire dati a WMI

WMI rende disponibili i dati Windows oggetti gestibili tramite [*i*](gloss-p.md)provider WMI . Un provider recupera i dati da un componente di sistema, ad esempio un processo o un'applicazione instrumentata, ad esempio SNMP o IIS, e li passa tramite WMI a un'applicazione di gestione. Ad esempio, quando un'applicazione o uno script richiede informazioni sul processo usando la classe [**WMI Win32 \_ Process,**](/windows/desktop/CIMWin32Prov/win32-process) i dati vengono ottenuti dinamicamente tramite un provider preinstallato.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Creazione di un modello per un oggetto gestibile](#creating-a-model-for-a-manageable-object)
-   [Implementazione di un modello per un oggetto gestibile](#implementing-a-model-for-a-manageable-object)
-   [Determinazione di un tipo di provider da implementare](#determining-a-provider-type-to-implement)
-   [Determinazione di un modello di hosting (implementazione) per un provider](#determining-a-hosting-implementation-model-for-a-provider)
-   [Implementazione di un provider](#implementing-a-provider)
-   [Registrazione di un provider con WMI e il sistema](#registering-a-provider-with-wmi-and-the-system)
-   [Test di un provider](#testing-a-provider)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>Creazione di un modello per un oggetto gestibile

Prima di sviluppare un provider, creare un modello di dati per rappresentare l'oggetto gestibile da esporre tramite WMI. Si pianificano gli oggetti dati che verranno esposti dal provider. Ad esempio, se si prevede di gestire la risoluzione dello schermo dello sfondo del desktop, è necessario decidere come modellare il desktop in un file [*Managed Object Format (MOF).*](gloss-m.md)

Per creare un modello utile:

-   Determinare gli scenari reali e modellare le informazioni che un cliente potrebbe voler leggere e aggiornare (ad esempio, modificando l'immagine di sfondo) per ogni oggetto gestibile. Queste sono le proprietà della classe.
-   Determinare il tipo di azioni che un cliente può voler eseguire con ogni oggetto gestibile. Questi sono i metodi.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implementazione di un modello per un oggetto gestibile

Per implementare un modello per gli oggetti gestibili, creare un file MOF contenente una classe WMI che rappresenta ogni oggetto. Per altre informazioni sulla creazione di un file MOF per definire le classi WMI, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md) La registrazione del provider e delle relative classi è in genere inclusa nel file MOF, anche se è possibile usare [l'API COM](com-api-for-wmi.md) per creare classi e metodi. Per altre informazioni, vedere [Sviluppo di un provider WMI.](developing-a-wmi-provider.md)

> [!Note]  
> Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti siano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e si riavvia, usare l'istruzione del preprocessore [**\# pragma autorecover**](pragma-autorecover.md) nel file di Managed Object Format [*(MOF).*](gloss-m.md)

 

Dopo aver creato il file MOF, compilarlo usando lo [**strumentoMofcomp.exe**](mofcomp.md) file. In questo modo viene notificata la presenza di errori nel file MOF e viene aggiunta la classe WMI definita nel file MOF al [*repository WMI*](gloss-w.md) in modo che la classe possa essere utilizzata da un provider.

## <a name="determining-a-provider-type-to-implement"></a>Determinazione di un tipo di provider da implementare

WMI supporta un determinato numero di tipi di provider, che determinano la natura delle informazioni recapitate e le operazioni supportate dai provider.

I tipi di provider sono:

-   [*Provider di istanze*](gloss-i.md)
-   [*Provider di metodi*](gloss-m.md)
-   [*Provider di proprietà*](gloss-p.md)
-   Provider di classi
-   [*Provider di eventi*](gloss-e.md)
-   [*Provider di consumer di eventi*](gloss-e.md)
-   [*Provider di associazioni*](gloss-a.md)

La maggior parte dei provider sono provider di istanze e provider di metodi. Un provider di istanze è il provider più comune e fornisce le istanze di una determinata classe. Un provider di metodi implementa i metodi di una o più classi. Per altre informazioni sui tipi di provider, vedere [Sviluppo di un provider WMI.](developing-a-wmi-provider.md)

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Determinazione di un modello di hosting (implementazione) per un provider

I provider WMI sono file binari implementati come oggetti COM. Ciò significa che ogni provider dispone di un file DLL che può essere eseguito all'interno di un processo e di un contesto di sicurezza specifici. Questo è ciò che WMI fa riferimento al modello [*di hosting*](gloss-h.md). WMI offre diversi modi per ospitare i provider, ma l'approccio più comune consiste nell'usare il modello di provider accoppiato (in esecuzione nel processo WMI) nel contesto di sicurezza NetworkServiceHost. Un provider WMI può essere classificato come accoppiato o [*disaccoccodato.*](gloss-d.md)

Il termine provider accoppiato o disaccoccodato determina in quale processo host è in esecuzione il provider rispetto a WMI fornito WMIPRVSE.EXE processo. Una procedura consigliata consiste nel determinare se i dati di gestione esposti dal provider e l'API o l'applicazione su cui si basa sono sempre disponibili nel sistema o meno. Se l'API o l'applicazione su cui si basa il provider è sempre disponibile (in esecuzione nel sistema), il provider deve essere un provider accoppiato. In caso contrario, deve essere un provider disaccoccodato. Per altre informazioni sui modelli di hosting, vedere [Hosting e sicurezza del provider.](provider-hosting-and-security.md)

Per altre informazioni sulla creazione di un provider accoppiato, vedere Inserimento di dati in [WMI](supplying-data-to-wmi-by-writing-a-provider.md)scrivendo un provider e per informazioni sull'incorporamento di un provider disaccoccodato in un'applicazione, vedere [Incorporamento](incorporating-a-provider-in-an-application.md)di un provider in un'applicazione .

I provider accoppiati possono essere descritti come in-process (in-process) o out-of-process (out-of-process). Quando un provider accoppiato è un provider in-process, viene eseguito in un processo di hosting WMI WMIPRVSE.EXE condiviso e viene implementato come server in-process COM (.dll). Quando un provider è un provider out-of-process, viene avviato da WMI su richiesta di un client o di un evento, ma viene eseguito come processo separato e viene implementato come eseguibile (.exe).

## <a name="implementing-a-provider"></a>Implementazione di un provider

Un provider può essere implementato nei modi seguenti:

-   Uso della creazione guidata ATL in Visual Studio.

    La procedura guidata ATL genera il codice del provider che implementa un provider accoppiato. Quando si usa la Procedura guidata ATL, è possibile specificare che si vuole creare un modello di run-time del provider in-proc (.dll) o out-of-process (.exe).

-   Definizione di un oggetto COM per contenere il provider.

    Il codice del provider è scritto in C++. Per altre informazioni, vedere [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).

-   L'uso delle classi nello [**spazio dei nomi Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) nel .NET Framework per creare un provider usando codice gestito. Lo **spazio dei nomi System.Management.Instrumentation** non è più supportato.

    Questo processo crea un provider disaccoccodato.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Registrazione di un provider con WMI e il sistema

Prima di usare il provider da un consumer, è importante registrarlo con il sistema WMI e il sottosistema COM Windows.

Un file MOF può contenere più tipi di provider per le stesse classi. Lo stesso nome di provider viene registrato come, ad esempio, un'istanza o un provider di metodi. Per altre informazioni, vedere [Registrazione di un provider.](registering-a-provider.md)

## <a name="testing-a-provider"></a>Test di un provider

Quando il codice del provider viene registrato, è importante testare correttamente il provider usando il provider di consumer diversi, ad esempio script, codice gestito .NET e consumer C++.

Eseguire le attività seguenti per testare il provider:

-   Verificare che il provider venga caricato correttamente tramite il rilevamento delle notifiche degli eventi [**\_ \_ OperationEvent wmiprovider MSFT.**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) Questi eventi segnalano eventuali errori di caricamento del provider. Altre classi di risoluzione dei problemi che possono essere utili sono [**\_ ProcessStartTrace Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) e [**\_ Win32 ProcessStopTrace.**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) Per altre informazioni sulla risoluzione dei problemi relativi ai provider, vedere [Debugging Providers](debugging-providers.md) and Provider Configuration e [Troubleshooting Classes.](provider-configuration-and-troubleshooting-classes.md)
-   Se il provider è un provider di istanza o di metodo, assicurarsi di testare ogni funzionalità del provider una alla volta per evitare confusione nel seguire la logica del codice.
-   Per un provider di istanze, creare un'applicazione client o uno script che richiama ogni interfaccia del provider (enumerazione, get, put ed delete). Anche se il provider non deve implementare alcun elemento, deve restituire un messaggio "non supportato". È possibile trovare i valori restituiti già definiti in [Codici restituiti WMI.](wmi-return-codes.md)
-   Per assicurarsi che il contesto di sicurezza desiderato funzioni come previsto, richiamare le operazioni supportate dal provider da un contesto di sicurezza non amministratore. Il provider deve supportare la rappresentazione. Se un utente privo delle credenziali di sicurezza corrette tenta di aggiornare i dati o di eseguire un'operazione che esegue un metodo, il provider deve negare l'accesso con il messaggio di errore appropriato.
-   Per altre informazioni sulla sicurezza del provider, vedere [Protezione del provider.](securing-your-provider.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hosting e sicurezza dei provider](provider-hosting-and-security.md)
</dt> <dt>

[Fornire dati a WMI scrivendo un provider](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Registrazione di un provider](registering-a-provider.md)
</dt> <dt>

[Risoluzione dei problemi relativi alle applicazioni client WMI](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Protezione del provider](securing-your-provider.md)
</dt> <dt>

[Recupero e fornitura di dati in una piattaforma a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
