---
description: Una classe di visualizzazione Unione è un'unione logica di istanze della classe di origine. Una classe di visualizzazione Unione include tutte le istanze delle classi di origine a meno che non si limitino le istanze includendo una clausola WHERE nella query di origine.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Creazione di una classe di visualizzazione Unione
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff9327645828c3db78a82811831f058cc27f202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317564"
---
# <a name="creating-a-union-view-class"></a><span data-ttu-id="b8474-104">Creazione di una classe di visualizzazione Unione</span><span class="sxs-lookup"><span data-stu-id="b8474-104">Creating a Union View Class</span></span>

<span data-ttu-id="b8474-105">Una classe di visualizzazione Unione è un'unione logica di istanze della classe di origine.</span><span class="sxs-lookup"><span data-stu-id="b8474-105">A union view class is a logical union of source class instances.</span></span> <span data-ttu-id="b8474-106">Una classe di visualizzazione Unione include tutte le istanze delle classi di origine a meno che non si limitino le istanze includendo una clausola WHERE nella query di origine.</span><span class="sxs-lookup"><span data-stu-id="b8474-106">A union view class includes all the instances of the source classes unless you limit the instances by including a WHERE clause on the source query.</span></span>

<span data-ttu-id="b8474-107">Le classi di visualizzazione Unione risultano utili quando si desidera visualizzare istanze di classi simili o identiche che si trovano in spazi dei nomi diversi o in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="b8474-107">Union view classes are useful when you want to see instances of similar or identical classes that are located in different namespaces or on different computers.</span></span> <span data-ttu-id="b8474-108">Ad esempio, è possibile creare una classe Union che contiene istanze di unità disco diverse da monitorare.</span><span class="sxs-lookup"><span data-stu-id="b8474-108">For example, you can create a union class that contains instances of different disk drives to monitor.</span></span>

<span data-ttu-id="b8474-109">È inoltre possibile basare le proprietà di una classe di visualizzazione Unione sulle proprietà non presenti in tutte le istanze della classe di origine.</span><span class="sxs-lookup"><span data-stu-id="b8474-109">You can also base the properties of a union view class on properties not present in all of the source class instances.</span></span> <span data-ttu-id="b8474-110">Se le istanze della classe di origine non hanno la stessa proprietà, le proprietà delle istanze della classe Union hanno un valore **null**.</span><span class="sxs-lookup"><span data-stu-id="b8474-110">If the source class instances do not have the same property, the properties of union class instances have a value of **NULL**.</span></span> <span data-ttu-id="b8474-111">Se, ad esempio, un'unità disco rigido ha una proprietà di **temperatura** , ma un'altra no, è comunque possibile creare un'unione tra i due.</span><span class="sxs-lookup"><span data-stu-id="b8474-111">For example, if one hard disk drive has a **temperature** property but another does not, you can still create a union between the two.</span></span>

<span data-ttu-id="b8474-112">Nella procedura riportata di seguito viene descritto come creare una classe di visualizzazione Unione.</span><span class="sxs-lookup"><span data-stu-id="b8474-112">The following procedure describes how to create a union view class.</span></span>

<span data-ttu-id="b8474-113">**Per creare una classe di visualizzazione Unione**</span><span class="sxs-lookup"><span data-stu-id="b8474-113">**To create a union view class**</span></span>

1.  <span data-ttu-id="b8474-114">Iniziare la definizione della classe con il qualificatore della stringa di [**Unione**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="b8474-114">Begin your class definition with the [**Union**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="b8474-115">I qualificatori [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association** e **Union** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="b8474-115">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="b8474-116">Creare le query che definiscono le classi di origine utilizzate nella classe di visualizzazione con il qualificatore [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="b8474-116">Create the queries that define source classes used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="b8474-117">Definire i nomi e il percorso degli spazi dei nomi in cui si trovano le classi di origine con il qualificatore [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="b8474-117">Define the names and location of the namespaces in which the source classes are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="b8474-118">Definire le proprietà che vengono mappate alle proprietà delle classi di origine con il qualificatore [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="b8474-118">Define the properties that map to the properties in the source classes with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="b8474-119">Se necessario, è possibile contrassegnare qualsiasi proprietà come appartenente a una classe di origine utilizzando il qualificatore [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="b8474-119">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="b8474-120">Definire le proprietà chiave delle classi di origine della classe di visualizzazione Unione.</span><span class="sxs-lookup"><span data-stu-id="b8474-120">Define the key properties of the source classes of your union view class.</span></span>

    <span data-ttu-id="b8474-121">Ogni classe di origine deve avere lo stesso numero di proprietà chiave corrispondenti a [**CimType**](swbemproperty-cimtype.md).</span><span class="sxs-lookup"><span data-stu-id="b8474-121">Each source class must have the same number of key properties matched by [**CIMType**](swbemproperty-cimtype.md).</span></span> <span data-ttu-id="b8474-122">Inoltre, le chiavi della classe di visualizzazione Unione devono identificare in modo univoco tutte le istanze di origine.</span><span class="sxs-lookup"><span data-stu-id="b8474-122">Also, the keys of your union view class must uniquely identify all source instances.</span></span> <span data-ttu-id="b8474-123">In alcuni casi, potrebbe essere necessario specificare le proprietà di sistema per assicurarsi che le istanze siano univoche.</span><span class="sxs-lookup"><span data-stu-id="b8474-123">In some cases, you might need to specify system properties to ensure that instances are unique.</span></span> <span data-ttu-id="b8474-124">Se, ad esempio, si crea una vista dall'Unione di due classi identiche in due spazi dei nomi diversi, è possibile includere la proprietà [**\_ \_ namespace**](--namespace.md) come chiave nella classe di visualizzazione per distinguere tra le due istanze.</span><span class="sxs-lookup"><span data-stu-id="b8474-124">For example, if you create a view from the union of two identical classes in two different namespaces, you could include the [**\_\_Namespace**](--namespace.md) property as a key in the view class to differentiate between the two instances.</span></span> <span data-ttu-id="b8474-125">Se si utilizzano due classi simili dello stesso spazio dei nomi per creare una vista, è possibile utilizzare la proprietà della **\_ \_ classe** per distinguere tra i due.</span><span class="sxs-lookup"><span data-stu-id="b8474-125">If you use two similar classes from the same namespace to create a view, you could use the **\_\_Class** property to distinguish between the two.</span></span> <span data-ttu-id="b8474-126">Rinominare le proprietà di sistema nella vista in modo da evitare un conflitto con le proprietà di sistema della classe di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b8474-126">Rename any system properties in the view so you can avoid a conflict with the system properties of the view class.</span></span>

6.  <span data-ttu-id="b8474-127">Definire i metodi desiderati utilizzando il qualificatore [**MethodSource**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="b8474-127">Define any methods you want using the [**MethodSource**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

    <span data-ttu-id="b8474-128">A differenza di altre classi di visualizzazione, è possibile creare metodi per modificare una vista Unione.</span><span class="sxs-lookup"><span data-stu-id="b8474-128">Unlike other view classes, you can create methods to modify a union view.</span></span>

<span data-ttu-id="b8474-129">Nell'esempio di codice seguente viene illustrata una classe di visualizzazione Union.</span><span class="sxs-lookup"><span data-stu-id="b8474-129">The following code example describes a union view class.</span></span>

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

 

 



