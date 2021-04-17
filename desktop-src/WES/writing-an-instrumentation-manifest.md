---
title: Scrittura di un manifesto di strumentazione
description: Le applicazioni e le dll usano un manifesto di strumentazione per identificare i provider di strumentazione e gli eventi scritti dai provider.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399062"
---
# <a name="writing-an-instrumentation-manifest"></a>Scrittura di un manifesto di strumentazione

Le applicazioni e le dll usano un manifesto di strumentazione per identificare i provider di strumentazione e gli eventi scritti dai provider. Un manifesto è un file XML che contiene gli elementi che identificano il provider. La convenzione prevede l'uso di. Man come estensione per il manifesto. Il manifesto deve essere conforme all'XSD del manifesto dell'evento. Per informazioni dettagliate sullo schema, vedere [schema EventManifest](eventmanifestschema-schema.md).

Un provider di strumentazione è qualsiasi applicazione o DLL che chiama le funzioni [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)o [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) per scrivere eventi in una sessione di traccia di [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) o in un canale del registro eventi. Un'applicazione può definire un singolo provider di strumentazione che copre tutti gli eventi che scrive oppure può definire un provider per l'applicazione e un provider per ogni dll. Il numero di provider definiti dall'applicazione nel manifesto dipende esclusivamente dal modo in cui l'applicazione desidera organizzare gli eventi che scrive.

Il vantaggio di specificare un provider per ogni DLL è che è quindi possibile abilitare e disabilitare i singoli provider e quindi gli eventi che generano. Questo vantaggio si applica solo se il provider è abilitato da una sessione di traccia ETW. Tutti gli eventi che specificano un canale del registro eventi vengono sempre scritti su tale canale.

Il manifesto deve identificare il provider e gli eventi che scrive, ma gli altri metadati, ad esempio canali, livelli e parole chiave, sono facoltativi. la definizione dei metadati facoltativi dipende da chi utilizzerà gli eventi. Se, ad esempio, gli amministratori o il personale di supporto utilizzano gli eventi utilizzando uno strumento come il Visualizzatore eventi Windows che legge gli eventi dai canali del registro eventi, è necessario definire i canali in cui vengono scritti gli eventi. Tuttavia, se il provider viene abilitato solo da una sessione di traccia ETW, non è necessario definire i canali.

Sebbene i metadati di livello, attività, OpCode e parole chiave siano facoltativi, è consigliabile usarli per raggruppare o raggruppare in modo logico gli eventi. Il raggruppamento degli eventi consente ai consumer di utilizzare solo gli eventi di interesse. Ad esempio, il consumer può eseguire una query per tutti gli eventi in cui Level è "Critical" e la parola chiave è "Write" oppure eseguire una query per tutti gli eventi scritti da un'attività specifica.

Oltre ai consumer che utilizzano il livello e le parole chiave per utilizzare tipi di eventi specifici, una sessione di traccia ETW può utilizzare i metadati di livello e parola chiave per indicare a ETW di limitare gli eventi scritti nel log di traccia eventi. Ad esempio, la sessione può limitare gli eventi solo agli eventi in cui il livello è "Error" o "Critical" e la parola chiave è "Read".

Un provider può definire i filtri utilizzati da una sessione per filtrare gli eventi in base ai dati dell'evento. Con il livello e le parole chiave, ETW determina se l'evento viene scritto nel log ma con i filtri, il provider usa i criteri dei dati del filtro per determinare se scrive l'evento nella sessione. I filtri sono applicabili solo quando una sessione di traccia ETW Abilita il provider.

Le sezioni seguenti illustrano come definire i componenti del manifesto:

-   [Identificazione del provider](identifying-the-provider.md)
-   [Definizione dei canali in cui vengono scritti gli eventi](defining-channels.md)
-   [Definizione dei livelli di gravità degli eventi scritti dal provider](defining-severity-levels.md)
-   [Definizione delle attività e delle operazioni eseguite dal provider](defining-tasks-and-opcodes.md)
-   [Definizione delle parole chiave che classificano gli eventi scritti dal provider](defining-keywords-used-to-classify-types-of-events.md)
-   [Definizione dei filtri utilizzati dal provider per filtrare gli eventi scritti](defining-filters.md)
-   [Definizione delle mappe nome/valore a cui fa riferimento i dati del modello](defining-name-value-mappings.md)
-   [Definizione dei modelli che definiscono i dati specifici dell'evento](defining-event-data-templates.md)
-   [Definizione degli eventi scritti dal provider](defining-events.md)

Sebbene sia possibile creare manualmente un manifesto di strumentazione, è consigliabile utilizzare lo strumento ECManGen.exe incluso nella \\ cartella bin del Windows SDK. Lo strumento ECManGen.exe usa un'interfaccia utente grafica che guida la creazione di un manifesto da zero senza dover usare tag XML. Conoscere le informazioni contenute in questa sezione e nella sezione [dello schema EventManifest](eventmanifestschema-schema.md) è utile quando si usa lo strumento.

Se si usa Visual Studio come editor XML, è possibile aggiungere lo schema [EventManifest](eventmanifestschema-schema.md) al progetto (vedere il menu XML) per sfruttare i vantaggi di IntelliSense, della convalida dello schema inline e di altre funzionalità per rendere la scrittura del manifesto semplice e accurata.

Dopo aver scritto il manifesto, usare il compilatore di messaggi per convalidare il manifesto e generare i file di risorse e di intestazione inclusi nel provider. Per altre informazioni, vedere [compilazione di un manifesto di strumentazione](compiling-an-instrumentation-manifest.md).

Nell'esempio seguente viene illustrata la struttura di un manifesto dell'evento completamente definito.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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



 

 