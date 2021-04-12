---
description: Viene descritta la sintassi di base di un'istruzione SELECT per le query di eventi.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Istruzione SELECT per le query di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233460"
---
# <a name="select-statement-for-event-queries"></a>Istruzione SELECT per le query di eventi

È possibile utilizzare un'ampia gamma di istruzioni SELECT per eseguire una query per le informazioni sugli eventi. Le istruzioni possono essere istruzioni di base oppure possono essere più restrittive per limitare il set di risultati restituito dalla query.

L'esempio seguente è un'istruzione SELECT di base utilizzata per eseguire una query per ottenere informazioni sugli eventi.


```sql
SELECT * FROM EventClass
```



Quando un consumer invia una query, si tratta di una richiesta di notifica di tutte le occorrenze dell'evento rappresentato da **EventClass**. Questa richiesta include una richiesta di notifica relativa a tutte le proprietà del sistema di eventi e non di sistema. Quando un provider di eventi invia una query, registra il supporto per la generazione di notifiche quando si verifica un evento rappresentato da **EventClass** .

I consumer possono specificare singole proprietà anziché l'asterisco ( \* ) nell'istruzione SELECT.

Nell'esempio seguente viene illustrato come eseguire una query per proprietà specifiche.


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



Tuttavia, tutte le proprietà di un oggetto incorporato vengono restituite, anche se la query specifica le proprietà dell'oggetto incorporato.

Nell'esempio seguente vengono illustrate due query che restituiscono gli stessi dati.


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



Se una proprietà di sistema non è pertinente per una query specifica, contiene **null**. Ad esempio, il valore della proprietà di sistema **\_ \_ RelPath** è **null** per tutte le query di eventi.

Le seguenti proprietà di sistema contengono **valori null** per le query di eventi:

<dl> \_\_Namespace  
\_\_Percorso  
\_\_RelPath  
\_\_Server  
</dl>

Per ulteriori informazioni, vedere [riferimento alle proprietà di sistema WMI](wmi-system-properties.md).

Tutte le query di evento possono includere una [clausola WHERE](where-clause.md)facoltativa, ma le clausole WHERE vengono utilizzate principalmente dai consumer per specificare filtri aggiuntivi. È vivamente consigliabile che i consumer specifichino sempre una clausola WHERE. Il costo di una query complessa è minimo rispetto al costo della distribuzione e dell'elaborazione delle notifiche non necessarie.

Nell'esempio seguente viene illustrata una query che richiede notifiche di tutti gli eventi di modifica dell'istanza che interessano la classe ipotetica **EmailEvent**.


```sql
SELECT * FROM EmailEvent
```



Se gli eventi associati a **EmailEvent** si verificano di frequente, il consumer viene invaso da eventi. Una query migliore richiede gli eventi solo quando determinate condizioni utilizzano proprietà della classe specificata, ad esempio quando il livello di importanza è elevato.

Nell'esempio seguente viene illustrata la query che è possibile usare se **EmailImportance** è una proprietà della classe **EmailEvent**.


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Si noti che WMI può rifiutare una query per diversi motivi. Ad esempio, la query può essere troppo complessa o con un utilizzo intensivo di risorse per la valutazione. Quando si verifica questa situazione, WMI restituisce codici di errore specifici, ad esempio la **\_ query WBEM E \_ non valida \_**.

È possibile utilizzare le proprietà degli oggetti incorporati nella clausola WHERE.

Nell'esempio seguente viene illustrato come eseguire una query per gli oggetti in cui la proprietà **TargetInstance** della classe di sistema [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) è un oggetto [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) incorporato e **FreeSpace** è una proprietà di **Win32 \_ disco logico**.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Esempio

L' [evento di creazione del monitoraggio per](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) un esempio di nome di processo specifico VBScript in TechNet utilizza l'istruzione SELECT per monitorare gli eventi di creazione dell'istanza WMI per \_ il processo Win32, filtrando il nome di un processo specifico.

 

 
