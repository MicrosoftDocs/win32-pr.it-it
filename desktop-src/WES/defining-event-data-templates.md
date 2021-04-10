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
# <a name="defining-event-data-templates"></a><span data-ttu-id="5729a-103">Definizione di modelli di dati degli eventi</span><span class="sxs-lookup"><span data-stu-id="5729a-103">Defining Event Data Templates</span></span>

<span data-ttu-id="5729a-104">I provider utilizzano i modelli di dati per definire i dati specifici degli eventi che includono con un evento e per definire i dati del filtro che una sessione di traccia ETW può passare al provider quando Abilita il provider.</span><span class="sxs-lookup"><span data-stu-id="5729a-104">Providers use data templates to define the event-specific data that they include with an event and to define the filter data that an ETW tracing session can pass to the provider when it enables the provider.</span></span> <span data-ttu-id="5729a-105">Se l'evento non include dati specifici dell'evento, non sarà possibile definire un modello.</span><span class="sxs-lookup"><span data-stu-id="5729a-105">If the event does not include event-specific data, you will not define a template.</span></span> <span data-ttu-id="5729a-106">Per definire un modello, usare l'elemento **template** .</span><span class="sxs-lookup"><span data-stu-id="5729a-106">To define a template, use the **template** element.</span></span> <span data-ttu-id="5729a-107">Un modello include un elemento di dati per ogni parte di dati inclusa nel provider con l'evento.</span><span class="sxs-lookup"><span data-stu-id="5729a-107">A template includes a data item for each piece of data that the provider includes with the event.</span></span> <span data-ttu-id="5729a-108">È possibile specificare tipi integrali, stringhe, matrici e strutture.</span><span class="sxs-lookup"><span data-stu-id="5729a-108">You can specify integral types, strings, arrays, and structures.</span></span> <span data-ttu-id="5729a-109">È necessario scrivere i dati dell'evento nell'ordine in cui sono stati definiti gli elementi di dati nel modello.</span><span class="sxs-lookup"><span data-stu-id="5729a-109">You must write the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="5729a-110">È anche possibile includere nel modello un frammento XML che i consumer devono usare per determinare come eseguire il rendering dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5729a-110">You can also include in the template, an XML fragment that consumers should use to determine how to render the event data.</span></span> <span data-ttu-id="5729a-111">Se non si include il frammento, i consumer devono eseguire il rendering dei dati dell'evento nell'ordine in cui sono stati definiti gli elementi di dati nel modello.</span><span class="sxs-lookup"><span data-stu-id="5729a-111">If you do not include the fragment, consumers should render the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="5729a-112">Quando si definisce un modello, è necessario assegnargli un identificatore di modello da usare per fare riferimento al modello in una definizione di evento.</span><span class="sxs-lookup"><span data-stu-id="5729a-112">When you define a template, you must give it a template identifier that you use to reference the template in an event definition.</span></span> <span data-ttu-id="5729a-113">Ogni elemento di dati nel modello deve specificare un nome e un tipo di dati di input (per un elenco di tipi di input, vedere la sezione Osservazioni del tipo complesso [**InputType**](eventmanifestschema-inputtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="5729a-113">Each data item in the template must specify a name and input data type (for a list of input types, see the Remarks section of the [**InputType**](eventmanifestschema-inputtype-complextype.md) complex type).</span></span> <span data-ttu-id="5729a-114">Se è possibile eseguire il rendering del tipo di dati di input in più formati, è necessario specificare il tipo di dati di output che indica ai consumer come eseguire il rendering dell'elemento dati.</span><span class="sxs-lookup"><span data-stu-id="5729a-114">If the input data type can be rendered in multiple formats, you should specify the output data type that tells consumers how to render the data item.</span></span> <span data-ttu-id="5729a-115">È ad esempio possibile eseguire il rendering di un tipo di dati di input UInt32 come un Unsigned Integer, un identificatore di thread, un indirizzo IPv4 e un codice di errore Win32 tra gli altri.</span><span class="sxs-lookup"><span data-stu-id="5729a-115">For example, an UInt32 input data type can be rendered as an unsigned integer, thread identifier, IPv4 address, and Win32 error code among others.</span></span> <span data-ttu-id="5729a-116">Se non si specifica il tipo di dati di output, i consumer devono utilizzare il tipo di output predefinito del tipo di input per eseguire il rendering dell'elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="5729a-116">If you do not specify the output data type, consumers should use the input type's default output type to render the data item.</span></span>

<span data-ttu-id="5729a-117">Per specificare una matrice, includere l'attributo **count** sull'elemento dati e impostarlo sul numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="5729a-117">To specify an array, include the **count** attribute on the data item and set it to the number of elements in the array.</span></span> <span data-ttu-id="5729a-118">La matrice può essere una matrice di dimensioni variabili o una matrice a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="5729a-118">The array can be a variable size array or fixed size array.</span></span> <span data-ttu-id="5729a-119">Se la matrice è di dimensioni fisse, impostare **count** sulla dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="5729a-119">If the array is a fixed size array, set **count** to the size of the array.</span></span> <span data-ttu-id="5729a-120">Se, ad esempio, una matrice di numeri interi ha una dimensione fissa di 10, impostare **count** su 10.</span><span class="sxs-lookup"><span data-stu-id="5729a-120">For example, if an array of integers has a fixed size of 10, set **count** to 10.</span></span> <span data-ttu-id="5729a-121">Quando si scrive la matrice, è necessario scrivere 40 byte di dati.</span><span class="sxs-lookup"><span data-stu-id="5729a-121">When you write the array, you must write 40 bytes of data.</span></span>

<span data-ttu-id="5729a-122">Se la matrice è una matrice di dimensioni variabili, impostare **count** sul nome dell'elemento dati che contiene la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="5729a-122">If the array is a variable size array, set **count** to the name of the data item that contains the size of the array.</span></span> <span data-ttu-id="5729a-123">Se la matrice contiene puntatori, l'indirizzo dei puntatori viene scritto come dati dell'evento e non per i dati a cui puntano i puntatori.</span><span class="sxs-lookup"><span data-stu-id="5729a-123">If the array contains pointers, the address of the pointers are written as the event data, not the data to which the pointers point.</span></span>

<span data-ttu-id="5729a-124">È necessario specificare l'attributo **length** se l'elemento dati è un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="5729a-124">You must specify the **length** attribute if the data item is a binary blob.</span></span> <span data-ttu-id="5729a-125">È inoltre possibile specificare l'attributo **length** per le stringhe a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="5729a-125">You can also specify the **length** attribute for fixed length strings.</span></span>

<span data-ttu-id="5729a-126">Specificare l'attributo **Map** se l'elemento dati rappresenta un valore di enumerazione e si desidera che il consumer stampi una stringa per il valore anziché il valore stesso.</span><span class="sxs-lookup"><span data-stu-id="5729a-126">Specify the **map** attribute if the data item represents an enumeration value and you want the consumer to print a string for the value instead of the value itself.</span></span>

<span data-ttu-id="5729a-127">Se si includono strutture nel modello, è necessario scrivere singolarmente i membri della struttura anziché scrivere la struttura, a meno che non sia possibile garantire l'allineamento dei limiti a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="5729a-127">If you include structures in the template, you should write the members of the structure individually instead of writing the structure unless you can guarantee 8-byte boundary alignment.</span></span>

<span data-ttu-id="5729a-128">È necessario considerare attentamente le informazioni incluse negli eventi, soprattutto quando gli eventi vengono scritti nei canali globali.</span><span class="sxs-lookup"><span data-stu-id="5729a-128">You should carefully consider the information that you include in the events, especially when the events are written into the global channels.</span></span> <span data-ttu-id="5729a-129">Come regola generale, è consigliabile non includere le informazioni private negli eventi.</span><span class="sxs-lookup"><span data-stu-id="5729a-129">As a general rule, you should not include private information in the events.</span></span> <span data-ttu-id="5729a-130">Sono incluse le password in testo non crittografato e le informazioni personali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5729a-130">This includes plaintext passwords and personal user information.</span></span> <span data-ttu-id="5729a-131">Inoltre, i programmi eseguiti dall'utente, gli URL visitati dall'utente e altre informazioni relative alle attività utente nel computer devono essere considerati privati.</span><span class="sxs-lookup"><span data-stu-id="5729a-131">Additionally, programs run by the user, URLs that the user visited, and other information related to the user activities on the computer should be considered private.</span></span>

<span data-ttu-id="5729a-132">Se è necessario registrare gli URL e i nomi utente negli eventi, non scriverli nei canali Windows (sistema e applicazione), perché questi canali sono leggibili da tutti gli utenti autenticati.</span><span class="sxs-lookup"><span data-stu-id="5729a-132">If you must record URLs and user names in the events, do not write them to the Windows channels (System and Application) because these channels are readable by all authenticated users.</span></span> <span data-ttu-id="5729a-133">Scriverli invece nei canali operativi o analitici.</span><span class="sxs-lookup"><span data-stu-id="5729a-133">Instead, write them to your own Operational or Analytic channels.</span></span> <span data-ttu-id="5729a-134">Impostare le autorizzazioni di accesso su questi canali per consentire solo agli amministratori di leggere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="5729a-134">Set the access permissions on these channels to allow only administrators to read the events.</span></span> <span data-ttu-id="5729a-135">Potrebbe essere necessario fornire una divulgazione appropriata per informare gli utenti del fatto che le informazioni private vengono rese disponibili agli amministratori.</span><span class="sxs-lookup"><span data-stu-id="5729a-135">You may need to provide an appropriate disclosure to notify users of the fact that private information is made available to the administrators.</span></span>

<span data-ttu-id="5729a-136">Nell'esempio seguente viene illustrato come definire un modello.</span><span class="sxs-lookup"><span data-stu-id="5729a-136">The following example shows how to define a template.</span></span> <span data-ttu-id="5729a-137">È necessario specificare l'attributo **TID** del modello a cui si fa riferimento nella definizione dell'evento o nella definizione del filtro.</span><span class="sxs-lookup"><span data-stu-id="5729a-137">You must specify the template's **tid** attribute that you reference in the event definition or filter definition.</span></span>


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
