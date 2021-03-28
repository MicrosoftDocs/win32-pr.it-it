---
description: I provider classici devono usare Managed Object Format (MOF) per pubblicare il layout dei dati degli eventi. I consumer possono quindi leggere il layout pubblicato da WMI in fase di esecuzione e usarlo per leggere i dati dell'evento.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Pubblicazione dello schema di eventi per un provider classico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343881"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a><span data-ttu-id="11242-104">Pubblicazione dello schema di eventi per un provider classico</span><span class="sxs-lookup"><span data-stu-id="11242-104">Publishing Your Event Schema for a Classic Provider</span></span>

<span data-ttu-id="11242-105">I provider [classici](about-event-tracing.md) devono usare [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) per pubblicare il layout dei dati degli eventi.</span><span class="sxs-lookup"><span data-stu-id="11242-105">[Classic](about-event-tracing.md) providers should use [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) to publish the layout of their event data.</span></span> <span data-ttu-id="11242-106">I consumer possono quindi leggere il layout pubblicato da WMI in fase di esecuzione e usarlo per leggere i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="11242-106">Consumers can then read the published layout from WMI at runtime and use it to read the event data.</span></span>

<span data-ttu-id="11242-107">Se si utilizza MOF per pubblicare il layout dei dati dell'evento in WMI, in genere si creano i tre tipi di classi MOF seguenti nello \\ spazio dei nomi WMI radice:</span><span class="sxs-lookup"><span data-stu-id="11242-107">If you use MOF to publish the layout of your event data in WMI, you typically create the following three types of MOF classes in the root\\wmi namespace:</span></span>

-   [<span data-ttu-id="11242-108">Classe MOF del provider</span><span class="sxs-lookup"><span data-stu-id="11242-108">A provider MOF class</span></span>](#provider-mof-classes)
-   [<span data-ttu-id="11242-109">Una o più classi MOF di evento</span><span class="sxs-lookup"><span data-stu-id="11242-109">One or more event MOF classes</span></span>](#event-mof-classes)
-   [<span data-ttu-id="11242-110">Una o più classi MOF di tipo di evento</span><span class="sxs-lookup"><span data-stu-id="11242-110">One or more event type MOF classes</span></span>](#event-type-mof-classes)

## <a name="provider-mof-classes"></a><span data-ttu-id="11242-111">Classi MOF del provider</span><span class="sxs-lookup"><span data-stu-id="11242-111">Provider MOF classes</span></span>

<span data-ttu-id="11242-112">Se si pubblica il layout dei dati dell'evento, è necessario creare una classe MOF che identifichi il provider.</span><span class="sxs-lookup"><span data-stu-id="11242-112">If you publish the layout of your event data, you must create a MOF class that identifies your provider.</span></span> <span data-ttu-id="11242-113">Questa classe deve derivare dalla classe MOF **EventTrace** e deve essere vuota (nessuna proprietà o metodo).</span><span class="sxs-lookup"><span data-stu-id="11242-113">This class must derive from the **EventTrace** MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="11242-114">La classe deve includere anche il qualificatore **GUID** che identifica in modo univoco il provider.</span><span class="sxs-lookup"><span data-stu-id="11242-114">The class must also include the **Guid** qualifier which uniquely identifies the provider.</span></span> <span data-ttu-id="11242-115">Si tratta dello stesso GUID usato quando si chiama la funzione [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) per registrare il provider.</span><span class="sxs-lookup"><span data-stu-id="11242-115">This is the same GUID you use when you calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register your provider.</span></span>

## <a name="event-mof-classes"></a><span data-ttu-id="11242-116">Classi MOF di evento</span><span class="sxs-lookup"><span data-stu-id="11242-116">Event MOF classes</span></span>

<span data-ttu-id="11242-117">Una classe MOF dell'evento definisce una classe di eventi forniti dal provider.</span><span class="sxs-lookup"><span data-stu-id="11242-117">An event MOF class defines a class of events that the provider provides.</span></span> <span data-ttu-id="11242-118">Questa classe deriva dalla classe MOF del provider e deve essere vuota (nessuna proprietà o metodo).</span><span class="sxs-lookup"><span data-stu-id="11242-118">This class derives from the provider MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="11242-119">La classe deve includere anche il qualificatore **GUID** che identifica in modo univoco la classe degli eventi definiti dalle classi figlio.</span><span class="sxs-lookup"><span data-stu-id="11242-119">The class must also include the **Guid** qualifier which uniquely identifies the class of events that its child classes define.</span></span> <span data-ttu-id="11242-120">Il provider utilizza questo stesso GUID quando si imposta il membro **GUID** della struttura dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="11242-120">The provider uses this same GUID when setting the **Guid** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="event-type-mof-classes"></a><span data-ttu-id="11242-121">Classi MOF di tipo evento</span><span class="sxs-lookup"><span data-stu-id="11242-121">Event type MOF classes</span></span>

<span data-ttu-id="11242-122">Una classe MOF di tipo evento definisce i dati effettivi dell'evento.</span><span class="sxs-lookup"><span data-stu-id="11242-122">An event type MOF class defines the actual event data.</span></span> <span data-ttu-id="11242-123">Questa classe deriva dalla classe MOF dell'evento padre.</span><span class="sxs-lookup"><span data-stu-id="11242-123">This class derives from its parent event MOF class.</span></span> <span data-ttu-id="11242-124">Quando si denomina la classe MOF del tipo di evento, la convenzione prevede l'uso del nome della classe MOF dell'evento all'inizio del nome della classe MOF del tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="11242-124">When naming the event type MOF class, the convention is to use the event MOF class name at the beginning of the event type MOF class name.</span></span> <span data-ttu-id="11242-125">Se, ad esempio, il nome della classe MOF dell'evento è HWConfig e la classe MOF del tipo di evento rappresenta le informazioni sulla CPU, è necessario denominare il tipo di evento MOF Class, HWConfig \_ CPU.</span><span class="sxs-lookup"><span data-stu-id="11242-125">For example, if the event MOF class name is HWConfig and the event type MOF class represents CPU information, you should name the event type MOF class, HWConfig\_CPU.</span></span>

<span data-ttu-id="11242-126">Usare il qualificatore **eventType** per la classe MOF del tipo di evento per identificare il tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="11242-126">Use the **EventType** qualifier on the event type MOF class to identify the event type.</span></span> <span data-ttu-id="11242-127">Se più tipi di evento utilizzano gli stessi dati di evento, è possibile utilizzare la stessa classe MOF.</span><span class="sxs-lookup"><span data-stu-id="11242-127">If multiple event types use the same event data, they can use the same MOF class.</span></span> <span data-ttu-id="11242-128">Il provider utilizza lo stesso valore del tipo di evento per identificare l'evento quando si imposta la **classe. tipo** membro della struttura dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="11242-128">The provider uses the same event type value to identify the event when setting the **Class.Type** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

<span data-ttu-id="11242-129">La classe MOF del tipo di evento contiene le proprietà.</span><span class="sxs-lookup"><span data-stu-id="11242-129">The event type MOF class contains properties.</span></span> <span data-ttu-id="11242-130">L'ordine di queste proprietà è quello di definire il layout dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="11242-130">The order of these properties define the layout of the event data.</span></span> <span data-ttu-id="11242-131">Nella tabella seguente vengono identificati i tipi di dati e i qualificatori che è possibile utilizzare per definire le proprietà.</span><span class="sxs-lookup"><span data-stu-id="11242-131">The following table identifies the data types and qualifiers you can use to define the properties.</span></span> <span data-ttu-id="11242-132">Per ulteriori informazioni sulla proprietà e sui qualificatori di classe che è possibile utilizzare, vedere la pagina relativa ai [qualificatori MOF di traccia eventi](event-tracing-mof-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="11242-132">For more information on the property and class qualifiers that you can use, see [Event Tracing MOF Qualifiers](event-tracing-mof-qualifiers.md).</span></span>



| <span data-ttu-id="11242-133">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="11242-133">Data type</span></span>              | <span data-ttu-id="11242-134">Qualificatori</span><span class="sxs-lookup"><span data-stu-id="11242-134">Qualifiers</span></span>                        | <span data-ttu-id="11242-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11242-135">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11242-136">**sint8**, **Uint8**</span><span class="sxs-lookup"><span data-stu-id="11242-136">**sint8**, **uint8**</span></span>   | <span data-ttu-id="11242-137">**Formato**</span><span class="sxs-lookup"><span data-stu-id="11242-137">**Format**</span></span>                        | <span data-ttu-id="11242-138">Dichiara un intero decimale a 1 byte.</span><span class="sxs-lookup"><span data-stu-id="11242-138">Declares a 1-byte decimal integer.</span></span> <span data-ttu-id="11242-139">Per dichiarare un carattere ANSI, utilizzare il qualificatore di **formato** e impostarne il valore su "c".</span><span class="sxs-lookup"><span data-stu-id="11242-139">To declare an ANSI character, use the **Format** qualifier and set its value to "c".</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="11242-140">**sint16**, **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11242-140">**sint16**, **uint16**</span></span> | <span data-ttu-id="11242-141">**Formato**</span><span class="sxs-lookup"><span data-stu-id="11242-141">**Format**</span></span>                        | <span data-ttu-id="11242-142">Dichiara un intero decimale a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="11242-142">Declares a 2-byte decimal integer.</span></span> <span data-ttu-id="11242-143">Per indicare che il numero è un numero esadecimale, utilizzare il qualificatore di **formato** .</span><span class="sxs-lookup"><span data-stu-id="11242-143">To indicate the number is a hexadecimal number, use the **Format** qualifier.</span></span> <span data-ttu-id="11242-144">Ad esempio, Format ("x").</span><span class="sxs-lookup"><span data-stu-id="11242-144">For example, format("x").</span></span>                                                                                                                                                                               |
| <span data-ttu-id="11242-145">**sint32**, **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11242-145">**sint32**, **uint32**</span></span> | <span data-ttu-id="11242-146">**Formato**</span><span class="sxs-lookup"><span data-stu-id="11242-146">**Format**</span></span>                        | <span data-ttu-id="11242-147">Dichiara un intero decimale a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="11242-147">Declares a 4-byte decimal integer.</span></span> <span data-ttu-id="11242-148">Per indicare che il numero è un numero esadecimale, utilizzare il qualificatore di **formato** e impostarne il valore su "x".</span><span class="sxs-lookup"><span data-stu-id="11242-148">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="11242-149">**sint64**, **UInt64**</span><span class="sxs-lookup"><span data-stu-id="11242-149">**sint64**, **uint64**</span></span> | <span data-ttu-id="11242-150">**Formato**</span><span class="sxs-lookup"><span data-stu-id="11242-150">**Format**</span></span>                        | <span data-ttu-id="11242-151">Dichiara un intero decimale a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="11242-151">Declares a 8-byte decimal integer.</span></span> <span data-ttu-id="11242-152">Per indicare che il numero è un numero esadecimale, utilizzare il qualificatore di **formato** e impostarne il valore su "x".</span><span class="sxs-lookup"><span data-stu-id="11242-152">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="11242-153">**boolean**</span><span class="sxs-lookup"><span data-stu-id="11242-153">**boolean**</span></span>            |                                   | <span data-ttu-id="11242-154">Dichiara un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="11242-154">Declares a Boolean value.</span></span> <span data-ttu-id="11242-155">Il consumer di eventi deve interpretare il valore come BOOL (Integer a 4 byte).</span><span class="sxs-lookup"><span data-stu-id="11242-155">The event consumer should interpret the value as BOOL (4-byte integer).</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="11242-156">**char16**</span><span class="sxs-lookup"><span data-stu-id="11242-156">**char16**</span></span>             |                                   | <span data-ttu-id="11242-157">Dichiara un carattere wide.</span><span class="sxs-lookup"><span data-stu-id="11242-157">Declares a wide character.</span></span> <span data-ttu-id="11242-158">Il consumer di eventi deve interpretare le matrici Char16 negli eventi del kernel come stringhe di caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="11242-158">The event consumer should interpret char16 arrays in kernel events as wide character strings.</span></span> <span data-ttu-id="11242-159">(Usare la dimensione della matrice per copiare la stringa.</span><span class="sxs-lookup"><span data-stu-id="11242-159">(Use the array size to copy the string.</span></span> <span data-ttu-id="11242-160">Alcune stringhe possono contenere caratteri NULL iniziali.</span><span class="sxs-lookup"><span data-stu-id="11242-160">Some strings may contain leading NULL characters.)</span></span>                                                                                                      |
| <span data-ttu-id="11242-161">**object**</span><span class="sxs-lookup"><span data-stu-id="11242-161">**object**</span></span>             | <span data-ttu-id="11242-162">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="11242-162">**Extension**</span></span>                     | <span data-ttu-id="11242-163">Dichiara un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="11242-163">Declares a binary blob.</span></span> <span data-ttu-id="11242-164">Il qualificatore di **estensione** indica il tipo di dati nel BLOB.</span><span class="sxs-lookup"><span data-stu-id="11242-164">The **Extension** qualifier indicates the type of data in the blob.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="11242-165">**string**</span><span class="sxs-lookup"><span data-stu-id="11242-165">**string**</span></span>             | <span data-ttu-id="11242-166">**Format**, **StringTermination**</span><span class="sxs-lookup"><span data-stu-id="11242-166">**Format**, **StringTermination**</span></span> | <span data-ttu-id="11242-167">Dichiara un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="11242-167">Declares a string value.</span></span> <span data-ttu-id="11242-168">Per indicare che la stringa è una stringa di caratteri wide, utilizzare il qualificatore di **formato** e impostarne il valore su "w".</span><span class="sxs-lookup"><span data-stu-id="11242-168">To indicate the string is a wide-character string use the **Format** qualifier and set its value to "w".</span></span> <span data-ttu-id="11242-169">Se non si specifica il qualificatore di **formato** , la stringa viene considerata una stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="11242-169">The string is considered an ANSI string if you do not specify the **Format** qualifier.</span></span> <span data-ttu-id="11242-170">Per indicare il modo in cui la stringa viene terminata, usare il qualificatore **StringTermination** .</span><span class="sxs-lookup"><span data-stu-id="11242-170">To indicate how the string is terminated, use the **StringTermination** qualifier.</span></span> <br/> |



 

<span data-ttu-id="11242-171">Per specificare una matrice, è possibile usare le parentesi quadre, \[ \] .</span><span class="sxs-lookup"><span data-stu-id="11242-171">To specify an array, you can use square brackets, \[\].</span></span> <span data-ttu-id="11242-172">Le parentesi quadre possono includere la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="11242-172">The square brackets can include the size of the array.</span></span> <span data-ttu-id="11242-173">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="11242-173">For example:</span></span>

`[WmiDataId(1), read] uint8 MyGuid[16];`

<span data-ttu-id="11242-174">È anche possibile usare il qualificatore **Max** per specificare le dimensioni di una matrice.</span><span class="sxs-lookup"><span data-stu-id="11242-174">You can also use the **Max** qualifier to specify the size of an array.</span></span> <span data-ttu-id="11242-175">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="11242-175">For example:</span></span>

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

<span data-ttu-id="11242-176">Se si includono le dimensioni della matrice tra parentesi quadre, il compilatore MOF genera automaticamente il qualificatore Max.</span><span class="sxs-lookup"><span data-stu-id="11242-176">If you include the size of the array in the square brackets, the MOF compiler generates the Max qualifier for you.</span></span>

<span data-ttu-id="11242-177">È importante usare il qualificatore **Description** per ogni proprietà.</span><span class="sxs-lookup"><span data-stu-id="11242-177">It is important that you use the **Description** qualifier for each property.</span></span> <span data-ttu-id="11242-178">La descrizione deve contenere un nome visualizzato che il consumer può utilizzare per la visualizzazione dei valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="11242-178">The description should contain a display name that the consumer can use when displaying the property values.</span></span>

<span data-ttu-id="11242-179">Nell'esempio seguente viene illustrato il contenuto di un file MOF che descrive un provider, un evento e un tipo di evento MOF Class.</span><span class="sxs-lookup"><span data-stu-id="11242-179">The following example shows the contents of a MOF file that describes a provider, event, and event type MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

<span data-ttu-id="11242-180">Si noti che i nomi di classe MOF del provider, dell'evento e del tipo di evento devono essere univoci all'interno dell'intero spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="11242-180">Note that the provider, event, and event type MOF class names must be unique within the entire namespace.</span></span> <span data-ttu-id="11242-181">Per evitare conflitti di denominazione, è necessario usare un nome univoco e descrittivo per tutti i nomi di classe.</span><span class="sxs-lookup"><span data-stu-id="11242-181">To avoid naming conflicts, you should use unique and descriptive name for all class names.</span></span> <span data-ttu-id="11242-182">Le proprietà della classe devono inoltre essere descrittive e univoche all'interno della relativa gerarchia di classi: una classe figlio che contiene lo stesso nome di proprietà di una classe padre sovrascrive la proprietà della classe padre.</span><span class="sxs-lookup"><span data-stu-id="11242-182">Class properties should also be descriptive and unique within its class hierarchy—a child class that contains the same property name as a parent class overwrites the property of the parent class.</span></span>

<span data-ttu-id="11242-183">Dopo aver definito le classi MOF, usare il compilatore MOF per generare lo schema di eventi e aggiungerlo al repository CIM.</span><span class="sxs-lookup"><span data-stu-id="11242-183">After defining your MOF classes, use the MOF compiler to generate your event schema and add it to the CIM repository.</span></span> <span data-ttu-id="11242-184">I consumer possono quindi leggere lo schema dal repository e leggere a livello di codice i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="11242-184">Consumers can then read the schema from the repository and programmatically read the event data.</span></span> <span data-ttu-id="11242-185">Per una descrizione completa della sintassi MOF e per l'uso del compilatore MOF (Mofcomp.exe) per aggiungere le classi MOF al repository CIM, vedere [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="11242-185">For a complete description of the MOF syntax and using the MOF compiler (Mofcomp.exe) to add your MOF classes to the CIM repository, see [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span></span> <span data-ttu-id="11242-186">Per informazioni sull'uso di Wbemtest.exe per accedere al repository CIM, vedere [Strumentazione gestione Windows](../wmisdk/wmi-start-page.md) (WMI).</span><span class="sxs-lookup"><span data-stu-id="11242-186">For information on using Wbemtest.exe to access the CIM repository, see [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).</span></span>

## <a name="versioning-mof-class"></a><span data-ttu-id="11242-187">Controllo delle versioni (classe MOF)</span><span class="sxs-lookup"><span data-stu-id="11242-187">Versioning MOF class</span></span>

<span data-ttu-id="11242-188">Se si aggiunge o si modifica una classe MOF del tipo di evento, la convenzione prevede la versione della classe MOF dell'evento e delle classi MOF del tipo di evento figlio.</span><span class="sxs-lookup"><span data-stu-id="11242-188">If you add or change an event type MOF class, the convention is to version both the event MOF class and its child event type MOF classes.</span></span> <span data-ttu-id="11242-189">Per eseguire la versione della classe MOF dell'evento corrente, aggiungere \_ VN al nome della classe, dove n è un numero incrementale a partire da 0.</span><span class="sxs-lookup"><span data-stu-id="11242-189">To version the current event MOF class, append \_Vn to the class name, where n is an incremental number starting at 0.</span></span> <span data-ttu-id="11242-190">Se questa è la prima revisione della classe, aggiungere \_ V0 al nome della classe.</span><span class="sxs-lookup"><span data-stu-id="11242-190">If this is the first revision to the class, append \_V0 to the class name.</span></span> <span data-ttu-id="11242-191">È inoltre necessario aggiungere il qualificatore **EventVersion** alla classe.</span><span class="sxs-lookup"><span data-stu-id="11242-191">You must also add the **EventVersion** qualifier to the class.</span></span> <span data-ttu-id="11242-192">Usare lo stesso numero di versione usato nel nome della classe per il valore del qualificatore **EventVersion** .</span><span class="sxs-lookup"><span data-stu-id="11242-192">Use the same version number you used in the class name for the value of the **EventVersion** qualifier.</span></span>

<span data-ttu-id="11242-193">La nuova versione della classe MOF dell'evento deve usare lo stesso nome e il qualificatore **GUID** della classe originale.</span><span class="sxs-lookup"><span data-stu-id="11242-193">The new version of the event MOF class must use the same name and **Guid** qualifier as the original class.</span></span> <span data-ttu-id="11242-194">La nuova classe può facoltativamente aggiungere il qualificatore **EventVersion** .</span><span class="sxs-lookup"><span data-stu-id="11242-194">The new class may optionally add the **EventVersion** qualifier.</span></span> <span data-ttu-id="11242-195">La classe MOF dell'evento che non contiene il qualificatore **EventVersion** è considerata la versione più recente o se tutte le versioni della classe contengono un qualificatore **EventVersion** , la classe con il numero di versione più alto viene considerata la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="11242-195">The event MOF class that does not contain the **EventVersion** qualifier is considered the latest version, or if all the versions of the class contain an **EventVersion** qualifier, then the class with the highest version number is considered the latest version.</span></span> <span data-ttu-id="11242-196">Il provider usa il membro **Class. Version** della struttura [**dell' \_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare la versione dell'evento incluso nella traccia.</span><span class="sxs-lookup"><span data-stu-id="11242-196">The provider uses the **Class.Version** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to identify the version of the event included in the trace.</span></span>

<span data-ttu-id="11242-197">Nell'esempio seguente viene illustrato come eseguire la versione di una classe MOF dell'evento.</span><span class="sxs-lookup"><span data-stu-id="11242-197">The following example shows how to version an event MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
