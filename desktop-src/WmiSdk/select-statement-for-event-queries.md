---
description: Viene descritta la sintassi di base di un'istruzione SELECT per le query di eventi.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Istruzione SELECT per query di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e36eaa8f396f8dd7b7c0b0c013d1d6738fefeb7ed2ae565ee7114ebb524faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315840"
---
# <a name="select-statement-for-event-queries"></a>Istruzione SELECT per query di eventi

È possibile usare un'ampia gamma di istruzioni SELECT per eseguire query per ottenere informazioni sugli eventi. Le istruzioni possono essere istruzioni di base o più restrittive per limitare il set di risultati restituito dalla query.

L'esempio seguente è un'istruzione SELECT di base utilizzata per eseguire una query per ottenere informazioni sugli eventi.


```sql
SELECT * FROM EventClass
```



Quando un consumer invia una query, è una richiesta di ricevere una notifica di tutte le occorrenze dell'evento rappresentato da **EventClass**. Questa richiesta include una richiesta di notifica su tutte le proprietà del sistema di eventi e non di sistema. Quando un provider di eventi invia una query, registra il supporto per la generazione di notifiche quando si verifica un evento rappresentato **da EventClass.**

I consumer possono specificare singole proprietà anziché l'asterisco ( \* ) nell'istruzione SELECT.

Nell'esempio seguente viene illustrato come eseguire una query per proprietà specifiche.


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



Tuttavia, vengono restituite tutte le proprietà di un oggetto incorporato, anche se la query specifica le proprietà dell'oggetto incorporato.

Nell'esempio seguente vengono illustrate due query che restituiscono gli stessi dati.


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



Se una proprietà di sistema non è pertinente per una query specifica, contiene **NULL.** Ad esempio, il valore della proprietà di sistema **\_ \_ RELPATH** è **NULL** per tutte le query di eventi.

Le proprietà di sistema seguenti contengono **NULL per** le query di eventi:

<dl> \_\_Namespace  
\_\_Percorso  
\_\_RelPath  
\_\_Server  
</dl>

Per altre informazioni, vedere Informazioni [di riferimento sulle proprietà di sistema WMI.](wmi-system-properties.md)

Tutte le query di evento possono includere una [clausola WHERE](where-clause.md)facoltativa, ma le clausole WHERE vengono usate principalmente dai consumer per specificare filtri aggiuntivi. È consigliabile che i consumer specificano sempre una clausola WHERE. Il costo di una query complessa è minimo rispetto al costo di recapito ed elaborazione di notifiche non richieste.

Nell'esempio seguente viene illustrata una query che richiede notifiche di tutti gli eventi di modifica dell'istanza che interessano l'ipotetica **classe EmailEvent**.


```sql
SELECT * FROM EmailEvent
```



Se gli eventi associati **a EmailEvent si** verificano di frequente, il consumer viene inondato di eventi. Una query migliore richiede gli eventi solo quando condizioni specifiche usano proprietà della classe specificata, ad esempio quando il livello di importanza è elevato.

Nell'esempio seguente viene illustrata la query che è possibile usare se **EmailImportance** è una proprietà della classe **EmailEvent**.


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Si noti che WMI può rifiutare una query per diversi motivi. Ad esempio, la query può essere troppo complessa o a elevato utilizzo di risorse per la valutazione. In questo caso, WMI restituisce codici di errore specifici, ad esempio **WBEM \_ E \_ INVALID \_ QUERY**.

Le proprietà degli oggetti incorporati possono essere utilizzate nella clausola WHERE.

L'esempio seguente illustra come eseguire una query per gli oggetti in cui la proprietà **TargetInstance** della classe di sistema [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) è un oggetto [**\_ Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) incorporato e **FreeSpace** è una proprietà di **Win32 \_ LogicalDisk.**


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Esempio

[L'evento](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) di creazione del monitoraggio per un nome di processo specifico di esempio VBScript in TechNet usa l'istruzione SELECT per monitorare gli eventi di creazione di istanze WMI per il processo Win32, filtrando in base a un \_ nome di processo specifico.

 

 
