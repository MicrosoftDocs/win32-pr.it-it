---
description: Un filtro eventi è una classe WMI che descrive gli eventi che WMI recapita a un consumer fisico.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Creazione di un filtro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319300"
---
# <a name="creating-an-event-filter"></a>Creazione di un filtro eventi

Un filtro eventi è una classe WMI che descrive gli eventi che WMI recapita a un consumer fisico. Ad esempio, un filtro eventi può indicare a WMI di recapitare a un consumer tutti gli eventi di risparmio energia o tutti gli eventi di riavvio del sistema. Un filtro eventi descrive inoltre le condizioni in base alle quali WMI recapita gli eventi. Un filtro eventi può specificare un evento intrinseco o estrinseco; e il filtro può fare riferimento a eventi che hanno origine nello spazio dei nomi, ovvero diversi dallo spazio dei nomi del filtro. Il consumer permanente deve avere lo stesso [**CreatorSID**](--eventconsumer.md) nelle istanze consumer, Filter e binding. Per altre informazioni, vedere [ricezione di eventi](receiving-events-securely.md)in modo sicuro.

Nella procedura seguente viene descritto come creare un filtro evento.

**Per creare un filtro eventi**

1.  Creare un'istanza della classe di sistema WMI [**\_ \_ EventFilter**](--eventfilter.md) .
2.  Creare un identificatore univoco per il filtro con la proprietà **Name** , in uno dei due modi seguenti:

    -   Usare uno schema privato.

        Il nome arbitrario dei filtri eventi funziona a condizione che non si verifichino conflitti con altri schemi di denominazione dei filtri. È necessario evitare conflitti di denominazione perché l'aggiunta di un'istanza con un valore di **nome** duplicato sovrascrive l'istanza precedente.

    -   Usare un identificatore univoco globale (GUID).

        Se si lascia il **nome** vuoto, WMI riempie il **nome** con un GUID.

3.  Descrivere il tipo di evento che si desidera filtrare con la proprietà di **query** .

    La proprietà **query** contiene la query WMI Query Language (WQL) che descrive il tipo di evento che si desidera filtrare. È possibile ottenere un filtro preciso utilizzando diversi operatori ed estensioni di WQL.

    Un evento di registro NT viene generato quando si verifica un errore in una query di un consumer di eventi permanenti. L'origine dell'evento è WinMgmt, l'ID evento è 10 e il tipo di evento è Error.

    WMI è più efficiente in fase di elaborazione di query restrittive e specifiche rispetto a query ampie. Creando una query specifica, è possibile evitare la comunicazione tra processi non necessaria e il traffico di rete. Nei casi di eventi generati da un provider, WMI esegue il filtro in corso per il provider. in questo modo si garantisce che solo gli eventi corrispondenti al filtro provochino il costo di comunicazione interprocesso. Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).

4.  Impostare la proprietà **QueryLanguage** sul tipo di linguaggio di query utilizzato nella proprietà **query** .

    Si imposta quasi sempre **QueryLanguage** su "WQL".

Nell'esempio di codice riportato di seguito viene descritto un filtro eventi che segnala un evento ogni volta che WMI crea un'istanza della classe [**\_ \_ TimerEvent**](--timerevent.md) nello \\ spazio dei nomi CIMV2 radice.

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

La proprietà **EventNamespace** specifica lo spazio dei nomi da cui hanno origine gli eventi. Non è necessario creare un'istanza dei filtri nello spazio dei nomi da cui hanno origine gli eventi. Se non si specifica lo spazio dei nomi, WMI crea il filtro nello spazio dei nomi predefinito. Le classi degli eventi intrinseci, ad esempio [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , sono disponibili in ogni spazio dei nomi.

Per registrare l'utente logico per le notifiche degli eventi, è necessario associare i filtri eventi a un consumer logico. Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md).

 

 



