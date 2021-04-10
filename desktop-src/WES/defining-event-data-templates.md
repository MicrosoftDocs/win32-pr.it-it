---
title: Definizione di modelli di dati degli eventi
description: I provider utilizzano i modelli di dati per definire i dati specifici degli eventi che includono con un evento e per definire i dati del filtro che una sessione di traccia ETW può passare al provider quando Abilita il provider.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067230472c8de5ce29145e221c109b3f390f0a6c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "103858094"
---
# <a name="defining-event-data-templates"></a>Definizione di modelli di dati degli eventi

I provider utilizzano i modelli di dati per definire i dati specifici degli eventi che includono con un evento e per definire i dati del filtro che una sessione di traccia ETW può passare al provider quando Abilita il provider. Se l'evento non include dati specifici dell'evento, non sarà possibile definire un modello. Per definire un modello, usare l'elemento **template** . Un modello include un elemento di dati per ogni parte di dati inclusa nel provider con l'evento. È possibile specificare tipi integrali, stringhe, matrici e strutture. È necessario scrivere i dati dell'evento nell'ordine in cui sono stati definiti gli elementi di dati nel modello.

È anche possibile includere nel modello un frammento XML che i consumer devono usare per determinare come eseguire il rendering dei dati dell'evento. Se non si include il frammento, i consumer devono eseguire il rendering dei dati dell'evento nell'ordine in cui sono stati definiti gli elementi di dati nel modello.

Quando si definisce un modello, è necessario assegnargli un identificatore di modello da usare per fare riferimento al modello in una definizione di evento. Ogni elemento di dati nel modello deve specificare un nome e un tipo di dati di input (per un elenco di tipi di input, vedere la sezione Osservazioni del tipo complesso [**InputType**](eventmanifestschema-inputtype-complextype.md) ). Se è possibile eseguire il rendering del tipo di dati di input in più formati, è necessario specificare il tipo di dati di output che indica ai consumer come eseguire il rendering dell'elemento dati. È ad esempio possibile eseguire il rendering di un tipo di dati di input UInt32 come un Unsigned Integer, un identificatore di thread, un indirizzo IPv4 e un codice di errore Win32 tra gli altri. Se non si specifica il tipo di dati di output, i consumer devono utilizzare il tipo di output predefinito del tipo di input per eseguire il rendering dell'elemento di dati.

Per specificare una matrice, includere l'attributo **count** sull'elemento dati e impostarlo sul numero di elementi nella matrice. La matrice può essere una matrice di dimensioni variabili o una matrice a dimensione fissa. Se la matrice è di dimensioni fisse, impostare **count** sulla dimensione della matrice. Se, ad esempio, una matrice di numeri interi ha una dimensione fissa di 10, impostare **count** su 10. Quando si scrive la matrice, è necessario scrivere 40 byte di dati.

Se la matrice è una matrice di dimensioni variabili, impostare **count** sul nome dell'elemento dati che contiene la dimensione della matrice. Se la matrice contiene puntatori, l'indirizzo dei puntatori viene scritto come dati dell'evento e non per i dati a cui puntano i puntatori.

È necessario specificare l'attributo **length** se l'elemento dati è un BLOB binario. È inoltre possibile specificare l'attributo **length** per le stringhe a lunghezza fissa.

Specificare l'attributo **Map** se l'elemento dati rappresenta un valore di enumerazione e si desidera che il consumer stampi una stringa per il valore anziché il valore stesso.

Se si includono strutture nel modello, è necessario scrivere singolarmente i membri della struttura anziché scrivere la struttura, a meno che non sia possibile garantire l'allineamento dei limiti a 8 byte.

È necessario considerare attentamente le informazioni incluse negli eventi, soprattutto quando gli eventi vengono scritti nei canali globali. Come regola generale, è consigliabile non includere le informazioni private negli eventi. Sono incluse le password in testo non crittografato e le informazioni personali dell'utente. Inoltre, i programmi eseguiti dall'utente, gli URL visitati dall'utente e altre informazioni relative alle attività utente nel computer devono essere considerati privati.

Se è necessario registrare gli URL e i nomi utente negli eventi, non scriverli nei canali Windows (sistema e applicazione), perché questi canali sono leggibili da tutti gli utenti autenticati. Scriverli invece nei canali operativi o analitici. Impostare le autorizzazioni di accesso su questi canali per consentire solo agli amministratori di leggere gli eventi. Potrebbe essere necessario fornire una divulgazione appropriata per informare gli utenti del fatto che le informazioni private vengono rese disponibili agli amministratori.

Nell'esempio seguente viene illustrato come definire un modello. È necessario specificare l'attributo **TID** del modello a cui si fa riferimento nella definizione dell'evento o nella definizione del filtro.


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
