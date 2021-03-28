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
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>Pubblicazione dello schema di eventi per un provider classico

I provider [classici](about-event-tracing.md) devono usare [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) per pubblicare il layout dei dati degli eventi. I consumer possono quindi leggere il layout pubblicato da WMI in fase di esecuzione e usarlo per leggere i dati dell'evento.

Se si utilizza MOF per pubblicare il layout dei dati dell'evento in WMI, in genere si creano i tre tipi di classi MOF seguenti nello \\ spazio dei nomi WMI radice:

-   [Classe MOF del provider](#provider-mof-classes)
-   [Una o più classi MOF di evento](#event-mof-classes)
-   [Una o più classi MOF di tipo di evento](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>Classi MOF del provider

Se si pubblica il layout dei dati dell'evento, è necessario creare una classe MOF che identifichi il provider. Questa classe deve derivare dalla classe MOF **EventTrace** e deve essere vuota (nessuna proprietà o metodo). La classe deve includere anche il qualificatore **GUID** che identifica in modo univoco il provider. Si tratta dello stesso GUID usato quando si chiama la funzione [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) per registrare il provider.

## <a name="event-mof-classes"></a>Classi MOF di evento

Una classe MOF dell'evento definisce una classe di eventi forniti dal provider. Questa classe deriva dalla classe MOF del provider e deve essere vuota (nessuna proprietà o metodo). La classe deve includere anche il qualificatore **GUID** che identifica in modo univoco la classe degli eventi definiti dalle classi figlio. Il provider utilizza questo stesso GUID quando si imposta il membro **GUID** della struttura dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

## <a name="event-type-mof-classes"></a>Classi MOF di tipo evento

Una classe MOF di tipo evento definisce i dati effettivi dell'evento. Questa classe deriva dalla classe MOF dell'evento padre. Quando si denomina la classe MOF del tipo di evento, la convenzione prevede l'uso del nome della classe MOF dell'evento all'inizio del nome della classe MOF del tipo di evento. Se, ad esempio, il nome della classe MOF dell'evento è HWConfig e la classe MOF del tipo di evento rappresenta le informazioni sulla CPU, è necessario denominare il tipo di evento MOF Class, HWConfig \_ CPU.

Usare il qualificatore **eventType** per la classe MOF del tipo di evento per identificare il tipo di evento. Se più tipi di evento utilizzano gli stessi dati di evento, è possibile utilizzare la stessa classe MOF. Il provider utilizza lo stesso valore del tipo di evento per identificare l'evento quando si imposta la **classe. tipo** membro della struttura dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

La classe MOF del tipo di evento contiene le proprietà. L'ordine di queste proprietà è quello di definire il layout dei dati dell'evento. Nella tabella seguente vengono identificati i tipi di dati e i qualificatori che è possibile utilizzare per definire le proprietà. Per ulteriori informazioni sulla proprietà e sui qualificatori di classe che è possibile utilizzare, vedere la pagina relativa ai [qualificatori MOF di traccia eventi](event-tracing-mof-qualifiers.md).



| Tipo di dati              | Qualificatori                        | Descrizione                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**, **Uint8**   | **Formato**                        | Dichiara un intero decimale a 1 byte. Per dichiarare un carattere ANSI, utilizzare il qualificatore di **formato** e impostarne il valore su "c".                                                                                                                                                                                                  |
| **sint16**, **UInt16** | **Formato**                        | Dichiara un intero decimale a 2 byte. Per indicare che il numero è un numero esadecimale, utilizzare il qualificatore di **formato** . Ad esempio, Format ("x").                                                                                                                                                                               |
| **sint32**, **UInt32** | **Formato**                        | Dichiara un intero decimale a 4 byte. Per indicare che il numero è un numero esadecimale, utilizzare il qualificatore di **formato** e impostarne il valore su "x".                                                                                                                                                                                |
| **sint64**, **UInt64** | **Formato**                        | Dichiara un intero decimale a 8 byte. Per indicare che il numero è un numero esadecimale, utilizzare il qualificatore di **formato** e impostarne il valore su "x".                                                                                                                                                                                |
| **boolean**            |                                   | Dichiara un valore booleano. Il consumer di eventi deve interpretare il valore come BOOL (Integer a 4 byte).                                                                                                                                                                                                                        |
| **char16**             |                                   | Dichiara un carattere wide. Il consumer di eventi deve interpretare le matrici Char16 negli eventi del kernel come stringhe di caratteri wide. (Usare la dimensione della matrice per copiare la stringa. Alcune stringhe possono contenere caratteri NULL iniziali.                                                                                                      |
| **object**             | **Estensione**                     | Dichiara un BLOB binario. Il qualificatore di **estensione** indica il tipo di dati nel BLOB.                                                                                                                                                                                                                              |
| **string**             | **Format**, **StringTermination** | Dichiara un valore stringa. Per indicare che la stringa è una stringa di caratteri wide, utilizzare il qualificatore di **formato** e impostarne il valore su "w". Se non si specifica il qualificatore di **formato** , la stringa viene considerata una stringa ANSI. Per indicare il modo in cui la stringa viene terminata, usare il qualificatore **StringTermination** . <br/> |



 

Per specificare una matrice, è possibile usare le parentesi quadre, \[ \] . Le parentesi quadre possono includere la dimensione della matrice. Ad esempio:

`[WmiDataId(1), read] uint8 MyGuid[16];`

È anche possibile usare il qualificatore **Max** per specificare le dimensioni di una matrice. Ad esempio:

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

Se si includono le dimensioni della matrice tra parentesi quadre, il compilatore MOF genera automaticamente il qualificatore Max.

È importante usare il qualificatore **Description** per ogni proprietà. La descrizione deve contenere un nome visualizzato che il consumer può utilizzare per la visualizzazione dei valori delle proprietà.

Nell'esempio seguente viene illustrato il contenuto di un file MOF che descrive un provider, un evento e un tipo di evento MOF Class.

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

Si noti che i nomi di classe MOF del provider, dell'evento e del tipo di evento devono essere univoci all'interno dell'intero spazio dei nomi. Per evitare conflitti di denominazione, è necessario usare un nome univoco e descrittivo per tutti i nomi di classe. Le proprietà della classe devono inoltre essere descrittive e univoche all'interno della relativa gerarchia di classi: una classe figlio che contiene lo stesso nome di proprietà di una classe padre sovrascrive la proprietà della classe padre.

Dopo aver definito le classi MOF, usare il compilatore MOF per generare lo schema di eventi e aggiungerlo al repository CIM. I consumer possono quindi leggere lo schema dal repository e leggere a livello di codice i dati dell'evento. Per una descrizione completa della sintassi MOF e per l'uso del compilatore MOF (Mofcomp.exe) per aggiungere le classi MOF al repository CIM, vedere [Managed Object Format](../wmisdk/managed-object-format--mof-.md). Per informazioni sull'uso di Wbemtest.exe per accedere al repository CIM, vedere [Strumentazione gestione Windows](../wmisdk/wmi-start-page.md) (WMI).

## <a name="versioning-mof-class"></a>Controllo delle versioni (classe MOF)

Se si aggiunge o si modifica una classe MOF del tipo di evento, la convenzione prevede la versione della classe MOF dell'evento e delle classi MOF del tipo di evento figlio. Per eseguire la versione della classe MOF dell'evento corrente, aggiungere \_ VN al nome della classe, dove n è un numero incrementale a partire da 0. Se questa è la prima revisione della classe, aggiungere \_ V0 al nome della classe. È inoltre necessario aggiungere il qualificatore **EventVersion** alla classe. Usare lo stesso numero di versione usato nel nome della classe per il valore del qualificatore **EventVersion** .

La nuova versione della classe MOF dell'evento deve usare lo stesso nome e il qualificatore **GUID** della classe originale. La nuova classe può facoltativamente aggiungere il qualificatore **EventVersion** . La classe MOF dell'evento che non contiene il qualificatore **EventVersion** è considerata la versione più recente o se tutte le versioni della classe contengono un qualificatore **EventVersion** , la classe con il numero di versione più alto viene considerata la versione più recente. Il provider usa il membro **Class. Version** della struttura [**dell' \_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare la versione dell'evento incluso nella traccia.

Nell'esempio seguente viene illustrato come eseguire la versione di una classe MOF dell'evento.

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

 

 
