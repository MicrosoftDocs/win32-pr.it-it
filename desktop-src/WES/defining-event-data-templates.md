---
title: Definizione dei modelli di dati degli eventi
description: I provider usano modelli di dati per definire i dati specifici dell'evento che includono con un evento e per definire i dati di filtro che una sessione di traccia ETW può passare al provider quando abilita il provider.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5480ca158916801665943bd33b886bfcd5d73015e8730c1dd108123dadc1995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652611"
---
# <a name="defining-event-data-templates"></a>Definizione dei modelli di dati degli eventi

I provider usano modelli di dati per definire i dati specifici dell'evento che includono con un evento e per definire i dati di filtro che una sessione di traccia ETW può passare al provider quando abilita il provider. Se l'evento non include dati specifici dell'evento, non si definirà un modello. Per definire un modello, usare **l'elemento del** modello. Un modello include un elemento dati per ogni parte di dati che il provider include con l'evento . È possibile specificare tipi integrali, stringhe, matrici e strutture. È necessario scrivere i dati dell'evento nell'ordine in cui gli elementi di dati sono stati definiti nel modello.

È anche possibile includere nel modello un frammento XML che i consumer devono usare per determinare come eseguire il rendering dei dati dell'evento. Se non si include il frammento, i consumer devono eseguire il rendering dei dati dell'evento nell'ordine in cui gli elementi di dati sono stati definiti nel modello.

Quando si definisce un modello, è necessario assegnargli un identificatore di modello da usare per fare riferimento al modello in una definizione di evento. Ogni elemento di dati nel modello deve specificare un nome e un tipo di dati di input (per un elenco di tipi di input, vedere la sezione Osservazioni del [**tipo complesso InputType).**](eventmanifestschema-inputtype-complextype.md) Se è possibile eseguire il rendering del tipo di dati di input in più formati, è necessario specificare il tipo di dati di output che indica ai consumer come eseguire il rendering dell'elemento di dati. È ad esempio possibile eseguire il rendering di un tipo di dati di input UInt32 come intero senza segno, identificatore di thread, indirizzo IPv4 e codice di errore Win32. Se non si specifica il tipo di dati di output, i consumer devono usare il tipo di output predefinito del tipo di input per eseguire il rendering dell'elemento di dati.

Per specificare una matrice, includere **l'attributo count** nell'elemento dati e impostarlo sul numero di elementi nella matrice. La matrice può essere una matrice di dimensioni variabili o una matrice di dimensioni fisse. Se la matrice è di dimensioni fisse, impostare **count** sulla dimensione della matrice. Ad esempio, se una matrice di numeri interi ha una dimensione fissa di 10, impostare **count** su 10. Quando si scrive la matrice, è necessario scrivere 40 byte di dati.

Se la matrice è una matrice di dimensioni variabili, impostare **count** sul nome dell'elemento di dati che contiene le dimensioni della matrice. Se la matrice contiene puntatori, l'indirizzo dei puntatori viene scritto come dati dell'evento, non i dati a cui puntano i puntatori.

È necessario specificare **l'attributo length** se l'elemento dati è un BLOB binario. È anche possibile specificare **l'attributo length** per le stringhe a lunghezza fissa.

Specificare **l'attributo map** se l'elemento di dati rappresenta un valore di enumerazione e si vuole che il consumer stampi una stringa per il valore anziché il valore stesso.

Se si includono strutture nel modello, è necessario scrivere i membri della struttura singolarmente anziché scrivere la struttura, a meno che non sia possibile garantire l'allineamento dei limiti a 8 byte.

È consigliabile considerare attentamente le informazioni incluse negli eventi, in particolare quando gli eventi vengono scritti nei canali globali. Come regola generale, non è consigliabile includere informazioni private negli eventi. Sono incluse le password in testo non crittografato e le informazioni utente personali. Inoltre, i programmi eseguiti dall'utente, gli URL visitati dall'utente e altre informazioni correlate alle attività dell'utente nel computer devono essere considerati privati.

Se è necessario registrare URL e nomi utente negli eventi, non scriverli nei canali Windows (Sistema e applicazione) perché questi canali sono leggibili da tutti gli utenti autenticati. Scriverli invece nei propri canali operativi o analitici. Impostare le autorizzazioni di accesso su questi canali per consentire solo agli amministratori di leggere gli eventi. Potrebbe essere necessario fornire una diffusione appropriata per informare gli utenti del fatto che le informazioni private vengono rese disponibili agli amministratori.

Nell'esempio seguente viene illustrato come definire un modello. È necessario specificare l'attributo **tid del** modello a cui si fa riferimento nella definizione dell'evento o del filtro.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
