---
description: I provider classici devono usare Managed Object Format (MOF) per pubblicare il layout dei dati degli eventi. I consumer possono quindi leggere il layout pubblicato da WMI in fase di esecuzione e usarlo per leggere i dati dell'evento.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Pubblicazione dello schema di eventi per un provider classico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e2e9b940df5afd6e8070e9235fe40566ef2b6d2b31b3c14656756835bab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069821"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>Pubblicazione dello schema di eventi per un provider classico

[I](about-event-tracing.md) provider classici devono [usare Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) per pubblicare il layout dei dati degli eventi. I consumer possono quindi leggere il layout pubblicato da WMI in fase di esecuzione e usarlo per leggere i dati dell'evento.

Se si usa MOF per pubblicare il layout dei dati degli eventi in WMI, in genere si creano i tre tipi di classi MOF seguenti nello spazio dei nomi \\ WMI radice:

-   [Classe MOF del provider](#provider-mof-classes)
-   [Una o più classi MOF di eventi](#event-mof-classes)
-   [Una o più classi MOF del tipo di evento](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>Classi MOF del provider

Se si pubblica il layout dei dati dell'evento, è necessario creare una classe MOF che identifica il provider. Questa classe deve derivare dalla **classe MOF EventTrace** e deve essere vuota (nessuna proprietà o metodo). La classe deve includere anche il **qualificatore Guid** che identifica in modo univoco il provider. Si tratta dello stesso GUID utilizzato quando si chiama la [**funzione RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) per registrare il provider.

## <a name="event-mof-classes"></a>Classi MOF di eventi

Una classe MOF di eventi definisce una classe di eventi forniti dal provider. Questa classe deriva dalla classe MOF del provider e deve essere vuota (nessuna proprietà o metodo). La classe deve includere anche il **qualificatore Guid** che identifica in modo univoco la classe di eventi definiti dalle classi figlio. Il provider usa lo stesso GUID quando imposta il **membro Guid** della struttura EVENT [**TRACE \_ \_ HEADER.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)

## <a name="event-type-mof-classes"></a>Classi MOF del tipo di evento

Una classe MOF del tipo di evento definisce i dati dell'evento effettivi. Questa classe deriva dalla classe MOF dell'evento padre. Quando si assegna un nome alla classe MOF del tipo di evento, la convenzione è usare il nome della classe MOF dell'evento all'inizio del nome della classe MOF del tipo di evento. Ad esempio, se il nome della classe MOF dell'evento è HWConfig e la classe MOF del tipo di evento rappresenta le informazioni sulla CPU, è necessario assegnare al tipo di evento il nome CLASSE MOF, CPU \_ HWConfig.

Usare il **qualificatore EventType** nella classe MOF del tipo di evento per identificare il tipo di evento. Se più tipi di evento usano gli stessi dati dell'evento, possono usare la stessa classe MOF. Il provider usa lo stesso valore del tipo di evento per identificare l'evento quando si imposta il membro **Class.Type** della [**struttura EVENT TRACE \_ \_ HEADER.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)

La classe MOF del tipo di evento contiene proprietà. L'ordine di queste proprietà definisce il layout dei dati dell'evento. La tabella seguente identifica i tipi di dati e i qualificatori che è possibile usare per definire le proprietà. Per altre informazioni sui qualificatori di proprietà e classi che è possibile usare, vedere [Qualificatori MOF di](event-tracing-mof-qualifiers.md)Traccia eventi .



| Tipo di dati              | Qualificatori                        | Descrizione                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**, **uint8**   | **Formato**                        | Dichiara un intero decimale a 1 byte. Per dichiarare un carattere ANSI, usare il **qualificatore Format** e impostarne il valore su "c".                                                                                                                                                                                                  |
| **sint16**, **uint16** | **Formato**                        | Dichiara un intero decimale a 2 byte. Per indicare che il numero è un numero esadecimale, usare il qualificatore **Format.** Ad esempio, format("x").                                                                                                                                                                               |
| **sint32**, **uint32** | **Formato**                        | Dichiara un intero decimale a 4 byte. Per indicare che il numero è un numero esadecimale, usare il qualificatore **Format** e impostarne il valore su "x".                                                                                                                                                                                |
| **sint64**, **uint64** | **Formato**                        | Dichiara un intero decimale a 8 byte. Per indicare che il numero è un numero esadecimale, usare il qualificatore **Format** e impostarne il valore su "x".                                                                                                                                                                                |
| **boolean**            |                                   | Dichiara un valore booleano. Il consumer di eventi deve interpretare il valore come BOOL (intero a 4 byte).                                                                                                                                                                                                                        |
| **char16**             |                                   | Dichiara un carattere wide. Il consumer di eventi deve interpretare le matrici char16 negli eventi del kernel come stringhe di caratteri wide. Usare le dimensioni della matrice per copiare la stringa. Alcune stringhe possono contenere caratteri NULL iniziali.                                                                                                      |
| **object**             | **Estensione**                     | Dichiara un BLOB binario. Il **qualificatore** di estensione indica il tipo di dati nel BLOB.                                                                                                                                                                                                                              |
| **string**             | **Format**, **StringTermination** | Dichiara un valore stringa. Per indicare che la stringa è una stringa di caratteri wide, usare il qualificatore **Format** e impostarne il valore su "w". La stringa viene considerata una stringa ANSI se non si specifica il **qualificatore Format.** Per indicare la modalità di terminazione della stringa, usare il **qualificatore StringTermination.** <br/> |



 

Per specificare una matrice, è possibile usare parentesi quadre, \[ \] . Le parentesi quadre possono includere le dimensioni della matrice. Esempio:

`[WmiDataId(1), read] uint8 MyGuid[16];`

È anche possibile usare il **qualificatore Max** per specificare le dimensioni di una matrice. Esempio:

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

Se si includono le dimensioni della matrice tra parentesi quadre, il compilatore MOF genera automaticamente il qualificatore Max.

È importante usare il qualificatore **Description** per ogni proprietà. La descrizione deve contenere un nome visualizzato che il consumer può usare per la visualizzazione dei valori delle proprietà.

Nell'esempio seguente viene illustrato il contenuto di un file MOF che descrive una classe MOF del provider, dell'evento e del tipo di evento.

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

Si noti che i nomi delle classi MOF del provider, dell'evento e del tipo di evento devono essere univoci all'interno dell'intero spazio dei nomi. Per evitare conflitti di denominazione, è necessario usare un nome univoco e descrittivo per tutti i nomi di classe. Le proprietà della classe devono anche essere descrittive e univoche all'interno della gerarchia di classi. Una classe figlio che contiene lo stesso nome di proprietà di una classe padre sovrascrive la proprietà della classe padre.

Dopo aver definito le classi MOF, usare il compilatore MOF per generare lo schema degli eventi e aggiungerlo al repository CIM. I consumer possono quindi leggere lo schema dal repository e leggere a livello di codice i dati dell'evento. Per una descrizione completa della sintassi MOF e dell'uso del compilatore MOF (Mofcomp.exe) per aggiungere le classi MOF al repository CIM, vedere [Managed Object Format](../wmisdk/managed-object-format--mof-.md). Per informazioni sull'Wbemtest.exe per accedere al repository CIM, vedere Windows [Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).

## <a name="versioning-mof-class"></a>Classe MOF di controllo delle versioni

Se si aggiunge o si modifica una classe MOF del tipo di evento, la convenzione è la versione della classe MOF dell'evento e delle classi MOF del tipo di evento figlio. Per eseguire la versione della classe MOF dell'evento corrente, aggiungere Vn al nome della classe, dove n è un numero \_ incrementale a partire da 0. Se si tratta della prima revisione della classe, aggiungere \_ V0 al nome della classe. È anche necessario aggiungere il **qualificatore EventVersion** alla classe . Usare lo stesso numero di versione usato nel nome della classe per il valore del **qualificatore EventVersion.**

La nuova versione della classe MOF dell'evento deve usare lo stesso nome e **qualificatore Guid** della classe originale. La nuova classe può facoltativamente aggiungere il **qualificatore EventVersion.** La classe MOF dell'evento che non contiene il qualificatore **EventVersion** viene considerata la versione più recente o se tutte le versioni della classe contengono un qualificatore **EventVersion,** la classe con il numero di versione più alto viene considerata la versione più recente. Il provider usa il **membro Class.Version** della [**struttura EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare la versione dell'evento incluso nella traccia.

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

 

 
