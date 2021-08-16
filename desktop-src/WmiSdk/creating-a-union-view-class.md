---
description: Una classe di visualizzazione unione è un'unione logica di istanze della classe di origine. Una classe di visualizzazione unione include tutte le istanze delle classi di origine, a meno che non si limitino le istanze includendo una clausola WHERE nella query di origine.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Creazione di una classe di visualizzazione unione
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3408e3aaec9ee809711b3f400c77ffab5ab2b376eaace3311bd0367f61937c30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612391"
---
# <a name="creating-a-union-view-class"></a>Creazione di una classe di visualizzazione unione

Una classe di visualizzazione unione è un'unione logica di istanze della classe di origine. Una classe di visualizzazione unione include tutte le istanze delle classi di origine, a meno che non si limitino le istanze includendo una clausola WHERE nella query di origine.

Le classi di visualizzazione unione sono utili quando si desidera visualizzare istanze di classi simili o identiche che si trovano in spazi dei nomi diversi o in computer diversi. Ad esempio, è possibile creare una classe unione che contiene istanze di unità disco diverse da monitorare.

È anche possibile basare le proprietà di una classe di visualizzazione unione su proprietà non presenti in tutte le istanze della classe di origine. Se le istanze della classe di origine non hanno la stessa proprietà, le proprietà delle istanze della classe di unione hanno un valore **NULL.** Ad esempio, se un'unità disco rigido ha una proprietà **temperature** ma un'altra no, è comunque possibile creare un'unione tra i due.

Nella procedura seguente viene descritto come creare una classe di visualizzazione unione.

**Per creare una classe di visualizzazione unione**

1.  Iniziare la definizione della classe con il [**qualificatore di stringa Union.**](qualifiers-specific-to-the-view-provider.md)

    I [**qualificatori JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association** e **Union** si escludono a vicenda.

2.  Creare le query che definiscono le classi di origine usate nella classe di visualizzazione con il [**qualificatore ViewSources.**](viewsources-qualifier.md)
3.  Definire i nomi e la posizione degli spazi dei nomi in cui si trovano le classi di origine con il [**qualificatore ViewSpaces.**](viewspaces-qualifier.md)
4.  Definire le proprietà mappate alle proprietà nelle classi di origine con il [**qualificatore PropertySources.**](propertysources-qualifier.md)

    Se necessario, è possibile contrassegnare qualsiasi proprietà come appartenente a una classe di origine usando il [**qualificatore HiddenDefault.**](qualifiers-specific-to-the-view-provider.md)

5.  Definire le proprietà chiave delle classi di origine della classe di visualizzazione unione.

    Ogni classe di origine deve avere lo stesso numero di proprietà chiave corrispondenti a [**CIMType.**](swbemproperty-cimtype.md) Inoltre, le chiavi della classe di visualizzazione unione devono identificare in modo univoco tutte le istanze di origine. In alcuni casi, potrebbe essere necessario specificare le proprietà di sistema per assicurarsi che le istanze siano univoche. Ad esempio, se si crea una vista dall'unione di due classi identiche in due spazi dei nomi diversi, è possibile includere la proprietà [**\_ \_ Namespace**](--namespace.md) come chiave nella classe di visualizzazione per distinguere le due istanze. Se si usano due classi simili dello stesso spazio dei nomi per creare una visualizzazione, è possibile usare la **\_ \_ proprietà Class** per distinguere le due classi. Rinominare le proprietà di sistema nella vista in modo da evitare conflitti con le proprietà di sistema della classe di visualizzazione.

6.  Definire i metodi desiderati usando il qualificatore [**MethodSource.**](qualifiers-specific-to-the-view-provider.md)

    A differenza di altre classi di visualizzazione, è possibile creare metodi per modificare una visualizzazione unione.

Nell'esempio di codice seguente viene descritta una classe di visualizzazione unione.

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 



