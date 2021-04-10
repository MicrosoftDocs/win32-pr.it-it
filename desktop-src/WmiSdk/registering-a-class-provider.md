---
description: Per creare un provider di classi WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ ClassProviderRegistration.
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: Registrazione di un provider di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15893e654f96f8c4e476219389a1f8f2c464a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967083"
---
# <a name="registering-a-class-provider"></a>Registrazione di un provider di classi

Per creare un provider di classi WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md). Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md). Se il provider archivia la maggior parte dei dati nel repository WMI e i dati vengono aggiornati solo nell'inizializzazione WMI, registrare la classe come provider di classi push. Se i dati che si forniscono cambiano di frequente e vengono recuperati in modo dinamico dal codice a ogni richiesta di WMI, registrare il provider come provider di classi pull.

Nella procedura seguente viene descritto come registrare un provider di classi push.

**Per registrare un provider di classi push**

-   Impostare la proprietà **InteractionType** dell'istanza [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) su 1.

    La creazione di un'istanza di [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) fa parte del processo di registrazione.

Nella procedura seguente viene descritto come registrare un provider di classi pull.

**Per registrare un provider di classi pull**

1.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.
2.  Creare un'istanza della classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) che descrive il set di funzionalità del provider.

    All'interno dell'istanza di [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) :

    1.  Impostare la proprietà **InteractionType** per indicare se il provider è un provider push o pull.
    2.  Contrassegnare la classe con i qualificatori [**dinamici**](standard-wmi-qualifiers.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .

        Il qualificatore [**dinamico**](standard-wmi-qualifiers.md) segnala che WMI deve usare un provider per recuperare le istanze della classe. Il qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) specifica il nome del provider che WMI deve utilizzare.

    3.  Definire le proprietà **ResultSetQueries**, **ReferencedSetQueries** e **UnsupportedQueries** .

        Queste proprietà di query descrivono informazioni dettagliate sulla classe supportata.

Oltre a descrivere i vari metodi supportati di una classe, la classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) dispone anche di tre proprietà che descrivono una serie di query. Se utilizzate insieme, queste tre proprietà descrivono l'intero intervallo di classi fornito dal provider di classi. Ogni proprietà di query contiene un'istruzione SELECT WQL, denominata "query dello schema", per specificare i tipi di classi supportate. Le query dello schema specificano un nome di classe speciale denominato meta \_ Class. Nella tabella seguente sono elencate le proprietà delle query.



| Proprietà                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ResultSetQueries**     | Contiene informazioni sul set di risultati fornito dal provider. WMI utilizza le informazioni per determinare se richiamare il provider per soddisfare una query da un'applicazione. Questa proprietà descrive il set di tutte le classi che possono essere fornite dal provider o un superset delle classi disponibili, ma mai un subset. WMI richiede che un provider specifichi almeno una query in questa proprietà.<br/> Nell'esempio seguente viene illustrato come impostare **ResultSetQueries** quando un provider fornisce una classe di associazione che fa riferimento alla classe [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> Nell'esempio seguente viene illustrato come specificare una query generale quando un provider fornisce classi che fanno riferimento ad altre classi sconosciute.<br/> `SELECT * FROM meta_class`<br/> Nell'esempio seguente viene illustrato come impostare **ResultSetQueries** quando un provider fornisce solo le sottoclassi, ma non la classe padre di una classe specificata.<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> Nell'esempio seguente viene illustrato come utilizzare \_ \_ questa proprietà speciale e impostare **ResultSetQueries** quando un provider fornisce tutte le classi e sottoclassi.<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **ReferencedSetQueries** | Determina se ignorare il provider nelle query dello schema in cui vengono richieste associazioni e riferimenti. I provider che possono fornire classi di associazione devono includere almeno una query nella relativa proprietà **ReferencedSetQueries** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **UnsupportedQueries**   | Contiene informazioni sul set di risultati non fornito da un provider di classi. WMI utilizza questa proprietà per sottrarre dal set di classi implicito da **ResultSetQueries**. Un provider di classi può ad esempio specificare nel supporto **ResultSetQueries** per tutte le classi derivate da MyClass e specificare in **UnsupportedQueries** una mancanza di supporto per una determinata classe derivata.<br/> Maggiori sono le informazioni che un provider è in grado di registrare sulle funzionalità di elaborazione delle query, più velocemente viene eseguito. L'immissione di una o più query nella proprietà **UnsupportedQueries** è un modo specifico ed è particolarmente importante quando un provider si basa su una classe non fornita. Quando viene effettuata una richiesta per una classe elencata in una query nella proprietà **UnsupportedQueries** , WMI può fornire la classe stessa o richiamare un provider alternativo per fornirla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Poiché WMI non supporta la clausola o, è necessario creare una query separata per ogni classe.

Le query seguenti vengono specificate in **ResultSetQueries** quando un provider di classi fornisce Class1, MyClass2 e MyClass3.


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



Solo gli amministratori possono registrare o eliminare un provider creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md).

 

