---
description: Per creare un provider di classi WMI, è necessario registrare \_ \_ l'istanza win32Provider che rappresenta il provider usando un'istanza di \_ \_ ClassProviderRegistration.
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: Registrazione di un provider di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16a28b489f2cfd01163d6b32c9a70c0d8a193a542197795d6d2b40de0e1baef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316483"
---
# <a name="registering-a-class-provider"></a>Registrazione di un provider di classi

Per creare un provider di classi WMI, è necessario registrare [**\_ \_ l'istanza win32Provider**](--win32provider.md) che rappresenta il provider usando un'istanza di [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md). Come oggetto COM, il provider deve registrarsi con il sistema operativo e WMI. La procedura seguente presuppone che il processo di registrazione sia già stato implementato come descritto in [Registrazione di un provider](registering-a-provider.md). Se il provider archivia la maggior parte dei dati nel repository WMI e i dati vengono aggiornati solo durante l'inizializzazione WMI, registrare la classe come provider di classi push. Se i dati che si forniscono frequentemente e vengono recuperati dinamicamente dal codice in ogni richiesta da WMI, registrare il provider come provider di classi pull.

La procedura seguente descrive come registrare un provider di classi push.

**Per registrare un provider di classi push**

-   Impostare la **proprietà InteractionType** dell'istanza [**\_ \_ classProviderRegistration**](--classproviderregistration.md) su 1.

    La creazione di [**\_ \_ un'istanza di ClassProviderRegistration**](--classproviderregistration.md) fa parte del processo di registrazione.

La procedura seguente descrive come registrare un provider di classi pull.

**Per registrare un provider di classi pull**

1.  Creare un'istanza della [**\_ \_ classe Win32Provider**](--win32provider.md) che descrive il provider.
2.  Creare un'istanza della [**\_ \_ classe ClassProviderRegistration**](--classproviderregistration.md) che descrive il set di funzionalità del provider.

    [**\_ \_ All'interno dell'istanza ClassProviderRegistration:**](--classproviderregistration.md)

    1.  Impostare la **proprietà InteractionType** per indicare se il provider è un provider push o pull.
    2.  Contrassegnare la classe con i [**qualificatori Dynamic**](standard-wmi-qualifiers.md) [**e Provider.**](/windows/desktop/api/Provider/nl-provider-provider)

        Il [**qualificatore dinamico**](standard-wmi-qualifiers.md) indica che WMI deve usare un provider per recuperare le istanze della classe. Il [**qualificatore**](/windows/desktop/api/Provider/nl-provider-provider) Provider specifica il nome del provider che DEVE essere utilizzato da WMI.

    3.  Definire le **proprietà ResultSetQueries**, **ReferencedSetQueries** e **UnsupportedQueries.**

        Queste proprietà di query descrivono informazioni dettagliate sulla classe supportata.

Oltre a descrivere i vari metodi supportati di una classe, la [**\_ \_ classe ClassProviderRegistration**](--classproviderregistration.md) include anche tre proprietà che descrivono una serie di query. Se usate insieme, queste tre proprietà descrivono l'intera gamma di classi fornite dal provider di classi. Ogni proprietà di query contiene un'istruzione SELECT WQL, denominata "query dello schema", per specificare i tipi di classi supportate. Le query dello schema specificano un nome di classe speciale denominato \_ metaclasse. Nella tabella seguente sono elencate le proprietà della query.



| Proprietà                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ResultSetQueries**     | Contiene informazioni sul set di risultati fornito dal provider. WMI usa le informazioni per determinare se richiamare il provider per soddisfare una query da un'applicazione. Questa proprietà descrive il set di tutte le classi che il provider può fornire o un superset delle classi disponibili, ma mai un subset. WMI richiede a un provider di specificare almeno una query in questa proprietà.<br/> Nell'esempio seguente viene illustrato come impostare **ResultSetQueries** quando un provider fornisce una classe di associazione che fa riferimento alla [**classe \_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> Nell'esempio seguente viene illustrato come specificare una query generale quando un provider fornisce classi che fanno riferimento ad altre classi sconosciute.<br/> `SELECT * FROM meta_class`<br/> Nell'esempio seguente viene illustrato come impostare **ResultSetQueries** quando un provider fornisce solo sottoclassi, ma non la classe padre di una determinata classe.<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> Nell'esempio seguente viene illustrato come usare la proprietà this speciale e \_ \_ impostare **ResultSetQueries** quando un provider fornisce tutte le classi e le sottoclassi.<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **ReferencedSetQueries** | Determina se ignorare il provider nelle query dello schema in cui vengono richieste associazioni e riferimenti. I provider che possono fornire classi di associazione devono includere almeno una query nella proprietà **ReferencedSetQueries.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Richieste non supportate**   | Contiene informazioni sul set di risultati non fornito da un provider di classi. WMI usa questa proprietà per sottrarre dal set di classi implicite **da ResultSetQueries**. Ad esempio, un provider di classi può specificare in **ResultSetQueries** il supporto per tutte le classi derivate da MyClass e specificare in **UnsupportedQueries** la mancanza di supporto per una classe derivata specifica.<br/> Maggiore è il numero di informazioni che un provider può registrare sulle funzionalità di elaborazione delle query, maggiore sarà la velocità di esecuzione. L'immissione di una o più query nella proprietà **UnsupportedQueries** è un modo per essere specifico ed è particolarmente importante quando un provider si basa su una classe che non fornisce. Quando viene effettuata una richiesta per una classe elencata in una query nella proprietà **UnsupportedQueries,** WMI può fornire la classe stessa o richiamare un provider alternativo per fornirla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Poiché WMI non supporta la clausola OR, è necessario creare una query separata per ogni classe.

Le query seguenti vengono specificate in **ResultSetQueries** quando un provider di classi fornisce MyClass1, MyClass2 e MyClass3.


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



Solo gli amministratori possono registrare o eliminare un provider creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md).

 

