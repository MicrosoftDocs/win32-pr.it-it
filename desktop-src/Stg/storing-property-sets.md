---
title: Archiviazione di set di proprietà
description: Le applicazioni possono esporre alcuni dati di stato dei documenti in modo che altre applicazioni possano individuare e leggere i dati.
ms.assetid: 2e0b5f6c-da1d-47f2-a50d-1ac7f2f0c45d
keywords:
- Archiviazione di set di proprietà di archiviazione strutturata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60710b84b52fcc709f8ba3ad1e930d6f5a50a4cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855597"
---
# <a name="storing-property-sets"></a>Archiviazione di set di proprietà

Le applicazioni possono esporre alcuni dati di stato dei documenti in modo che altre applicazioni possano individuare e leggere i dati. Alcuni esempi sono un set di proprietà che descrive l'autore, il titolo e le parole chiave di un documento creato con un elaboratore di testo o l'elenco dei tipi di carattere usati in un documento. Questa funzionalità non è limitata ai documenti; può inoltre essere utilizzato su oggetti incorporati. Generalmente, l'accesso ai set di proprietà deve essere eseguito tramite le interfacce [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , ma in questa sezione viene descritta la modalità consigliata in precedenza.

> [!Note]  
> Se si archivia un set di proprietà interno all'applicazione, è possibile che non si desideri utilizzare le linee guida seguenti. Per esporre la proprietà impostata ad altre applicazioni, attenersi alle indicazioni seguenti.

 

**Per archiviare un set di proprietà in un file composto**

1.  Creare un'istanza di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) nello stesso livello della struttura di archiviazione dei relativi flussi di dati. Seguire il nome dell'istanza di **IStorage** o **IStream** con " \\ 005". I nomi di flusso e archiviazione che iniziano con 0x05 sono riservati per i set di proprietà comuni che possono essere condivisi tra le applicazioni. Inoltre, i flussi che iniziano con tale valore sono limitati a 256 KB. I nomi possono essere selezionati da nomi e formati pubblicati oppure assegnando la proprietà impostare un FMTID e derivando il nome da FMTID in base alle convenzioni descritte in [convenzioni di denominazione degli oggetti di archiviazione](storage-object-naming-conventions.md).
2.  Un set di proprietà può essere archiviato in una singola istanza di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o in un'istanza di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) contenente più flussi e archivi. Nel caso di un'istanza di **IStorage** , il flusso contenuto denominato contenuto è il flusso primario che contiene i valori di proprietà, in cui alcuni valori possono essere nomi di altri flussi o istanze di archiviazione all'interno dello spazio di archiviazione per questo set di proprietà.
3.  Specificare il CLSID della classe di oggetti in grado di visualizzare o fornire l'accesso a livello di codice ai valori della proprietà. Se non esiste alcuna classe di questo tipo, è necessario impostare il CLSID sull'identificatore di formato del set di proprietà. Per un set di proprietà che usa un'istanza di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , impostare il CLSID dell'istanza di **IStorage** in modo che corrisponda a quello archiviato nel flusso di contenuto o a **CLSID \_ null**, ovvero il valore in un'istanza di **IStorage** appena creata.
4.  È possibile specificare nomi visualizzabili che formano il contenuto del dizionario.

Alcune applicazioni possono leggere solo le implementazioni dei set di proprietà archiviati come istanze [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) . Le applicazioni devono essere scritte in modo da prevedere che un set di proprietà possa essere archiviato in un'istanza di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o **IStream** , a meno che la definizione del set di proprietà non indichi diversamente. La definizione del set di proprietà informazioni di riepilogo, ad esempio, indica che può essere archiviata solo in un'istanza di **IStream** denominata. Nei casi in cui si sta cercando un set di proprietà e non si sa se si tratta di un'archiviazione o di un flusso, cercare prima un'istanza di **IStream** con il nome del set di proprietà. Se l'operazione ha esito negativo, cercare un'istanza di **IStorage** .

Per comprendere meglio l'archiviazione di set di proprietà in un'implementazione di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , si supponga di disporre di una classe di applicazioni che modificano le informazioni sugli animali. In primo luogo, viene definito un CLSID (CLSID \_ AnimalApp) per questo set di applicazioni, in modo da poter indicare che i set di proprietà che contengono informazioni sugli animali (**fmtid \_ AnimalInfo**) e altre contengono informazioni mediche (**fmtid \_ MedicalInfo**).

``` syntax
IStorage (File): "C:\OLE\REVO.DOC" 
  IStorage: "\005AnimalInfo", CLSID = CLSID_AnimalApp 
    IStream: "Contents" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = FMTID_AnimalInfo 
      Property: Type = PID_ANIMALTYPE, Type = VT_LPWSTR, 
              Value = L"Dog" 
      Property: Type = PID_ANIMALNAME, Type = VT_LPWSTR, 
              Value = L"Revo" 
      Property: Type = PID_MEDICALHISTORY, Type = VT_STREAMED_OBJECT, 
              Value = "MedicalInfo" 
      ... 
    IStream: "MedicalInfo" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = CLSID_MedicalInfo 
      Property: Type = PID_VETNAME, Type = VT_LPWSTR, 
              Value = L"Dr. Woof" 
      Property: Type = PID_LASTEXAM, Type = VT_DATE, Value = ...
```

Tenere presente che il CLSID dell'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e di entrambi i set di proprietà è **CLSID \_ AnimalApp**. Identifica qualsiasi applicazione in grado di visualizzare e/o fornire l'accesso programmatico a questi set di proprietà. Qualsiasi applicazione può leggere i dati all'interno dei set di proprietà (il punto dietro set di proprietà), ma solo le applicazioni identificate con l'identificatore di classe CLSID \_ AnimalApp possono comprendere il significato dei dati nei set di proprietà.

 

 




