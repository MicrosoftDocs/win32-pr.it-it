---
title: Scrittura di un manifesto di strumentazione
description: Le applicazioni e le DLL usano un manifesto di strumentazione per identificare i provider di strumentazione e gli eventi che i provider scrivono.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc832278772a12195590a4efdb7b65478f22ef4a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812169"
---
# <a name="writing-an-instrumentation-manifest"></a>Scrittura di un manifesto di strumentazione

Le applicazioni e le DLL usano un manifesto di strumentazione per identificare i provider di strumentazione e gli eventi che i provider scrivono. Un manifesto è un file XML che contiene gli elementi che identificano il provider. La convenzione è usare .man come estensione per il manifesto. Il manifesto deve essere conforme al manifesto dell'evento XSD. Per informazioni dettagliate sullo schema, vedere [Schema EventManifest](eventmanifestschema-schema.md).

Un provider di strumentazione è qualsiasi applicazione o DLL che chiama le funzioni [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)o [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) per scrivere eventi in una sessione di traccia ETW [(Event Tracing)](/windows/desktop/ETW/event-tracing-portal) o in un canale del registro eventi. Un'applicazione può definire un singolo provider di strumentazione che copre tutti gli eventi scritti oppure può definire un provider per l'applicazione e un provider per ogni DLL. Il numero di provider definiti dall'applicazione nel manifesto dipende esclusivamente dal modo in cui l'applicazione vuole organizzare gli eventi che scrive.

Il vantaggio di specificare un provider per ogni DLL è che è quindi possibile abilitare e disabilitare i singoli provider e quindi gli eventi generati. Questo vantaggio si applica solo se il provider è abilitato da una sessione di traccia ETW. Tutti gli eventi che specificano un canale del registro eventi vengono sempre scritti in tale canale.

Il manifesto deve identificare il provider e gli eventi che scrive, ma gli altri metadati, ad esempio canali, livelli e parole chiave, sono facoltativi. se si definiscono i metadati facoltativi dipende da chi utilizza gli eventi. Ad esempio, se gli amministratori o il personale di supporto usano gli eventi usando uno strumento come il Windows Visualizzatore eventi che legge gli eventi dai canali del registro eventi, è necessario definire i canali in cui vengono scritti gli eventi. Tuttavia, se il provider verrà abilitato solo da una sessione di traccia ETW, non è necessario definire i canali.

Anche se i metadati relativi a livelli, attività, codici opcode e parole chiave sono facoltativi, è consigliabile usarli per raggruppare o raggruppare in bucket logicamente gli eventi. Il raggruppamento degli eventi consente ai consumer di utilizzare solo gli eventi di interesse. Ad esempio, il consumer può eseguire una query per tutti gli eventi in cui level è "critical" e la parola chiave è "write" o query per tutti gli eventi scritti da un'attività specifica.

Oltre ai consumer che usano parole chiave e livelli per utilizzare tipi specifici di eventi, una sessione di traccia ETW può usare i metadati di livello e parola chiave per indicare a ETW di limitare gli eventi scritti nel log di traccia eventi. Ad esempio, la sessione potrebbe limitare gli eventi solo agli eventi in cui level è "error" o "critical" e la parola chiave è "read".

Un provider può definire filtri utilizzati da una sessione per filtrare gli eventi in base ai dati degli eventi. Con il livello e le parole chiave, ETW determina se l'evento viene scritto nel log, ma con i filtri, il provider usa i criteri dei dati di filtro per determinare se scrive l'evento in tale sessione. I filtri sono applicabili solo quando una sessione di traccia ETW abilita il provider.

Le sezioni seguenti illustrano come definire i componenti del manifesto:

-   [Identificazione del provider](identifying-the-provider.md)
-   [Definizione dei canali in cui vengono scritti gli eventi](defining-channels.md)
-   [Definizione dei livelli di gravità degli eventi scritti dal provider](defining-severity-levels.md)
-   [Definizione delle attività e delle operazioni eseguite dal provider](defining-tasks-and-opcodes.md)
-   [Definizione delle parole chiave che classificano gli eventi scritti dal provider](defining-keywords-used-to-classify-types-of-events.md)
-   [Definizione dei filtri utilizzati dal provider per filtrare gli eventi scritti](defining-filters.md)
-   [Definizione delle mappe nome/valore a cui fa riferimento il modello](defining-name-value-mappings.md)
-   [Definizione dei modelli che definiscono i dati specifici dell'evento](defining-event-data-templates.md)
-   [Definizione degli eventi scritti dal provider](defining-events.md)

Anche se è possibile creare manualmente un manifesto di strumentazione, è consigliabile usare lo strumento ECManGen.exe incluso nella cartella Bin di \\ Windows SDK. Lo ECManGen.exe usa un'interfaccia utente grafica che consente di creare un manifesto da zero senza dover usare tag XML. La conoscenza delle informazioni contenute in questa sezione e nella [sezione Schema EventManifest](eventmanifestschema-schema.md) sarà utile quando si usa lo strumento.

Se si usa Visual Studio come editor XML, è possibile aggiungere lo schema [EventManifest](eventmanifestschema-schema.md) al progetto (vedere il menu XML) per sfruttare i vantaggi di Intellisense, la convalida dello schema inline e altre funzionalità per semplificare e accuratezza la scrittura del manifesto.

Dopo aver scritto il manifesto, usare il compilatore di messaggi per convalidare il manifesto e generare i file di risorsa e di intestazione inclusi nel provider. Per altre informazioni, vedere [Compilazione di un manifesto di strumentazione](compiling-an-instrumentation-manifest.md).

L'esempio seguente illustra lo scheletro di un manifesto dell'evento completamente definito.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 
