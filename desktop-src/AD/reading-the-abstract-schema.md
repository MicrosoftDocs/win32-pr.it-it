---
title: Lettura dello schema astratto
description: In questo argomento vengono forniti un esempio di codice e linee guida per la lettura dallo schema astratto, che fornisce un subset dei dati archiviati negli oggetti attributeSchema e classSchema nel contenitore dello schema.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- schema Active Directory, lettura dello schema astratto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d7fadba33bcc5e93bf2b9e89934e8b440d559b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872258"
---
# <a name="reading-the-abstract-schema"></a><span data-ttu-id="6fbc6-104">Lettura dello schema astratto</span><span class="sxs-lookup"><span data-stu-id="6fbc6-104">Reading the Abstract Schema</span></span>

<span data-ttu-id="6fbc6-105">In questo argomento vengono forniti un esempio di codice e linee guida per la lettura dallo schema astratto, che fornisce un subset dei dati archiviati negli oggetti **attributeSchema** e **classSchema** nel contenitore dello schema.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-105">This topic provides a code example and guidelines for reading from the abstract schema, which provides a subset of the data stored in the **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="6fbc6-106">Per recuperare i dati non disponibili nello schema astratto, leggere i dati direttamente dal contenitore dello schema come descritto in [lettura degli oggetti attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6fbc6-106">To retrieve data that is unavailable in the abstract schema, read the data directly from the schema container as described in [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="6fbc6-107">Utilizzare la stringa di associazione "LDAP://schema" per eseguire il binding a un puntatore [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) nello schema astratto.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-107">Use the "LDAP://schema" binding string to bind to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the abstract schema.</span></span> <span data-ttu-id="6fbc6-108">Utilizzare questo puntatore per enumerare le voci relative a classi, attributi e sintassi nello schema astratto.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-108">Use this pointer to enumerate the class, attribute, and syntax entries in the abstract schema.</span></span> <span data-ttu-id="6fbc6-109">È anche possibile usare il metodo [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) per recuperare singole voci.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-109">You can also use the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to retrieve individual entries.</span></span>


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



<span data-ttu-id="6fbc6-110">Usare una stringa di associazione simile, "LDAP://schema/ <object> ", per eseguire l'associazione diretta a una voce di classe o attributo nello schema astratto.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-110">Use a similar binding string, "LDAP://schema/<object>", to bind directly to a class or attribute entry in the abstract schema.</span></span> <span data-ttu-id="6fbc6-111">In questa stringa " &lt; Object &gt; " è l' **ldapDisplayName** di una classe o di un attributo.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-111">In this string, "&lt;object&gt;" is the **lDAPDisplayName** of a class or attribute.</span></span> <span data-ttu-id="6fbc6-112">Per le classi sono associate all'interfaccia [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) ; per gli attributi, associare l'interfaccia [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) .</span><span class="sxs-lookup"><span data-stu-id="6fbc6-112">For classes bind to the [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) interface; for attributes, bind to [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) interface.</span></span>


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



<span data-ttu-id="6fbc6-113">Inoltre, l'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) fornisce la proprietà [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="6fbc6-113">In addition, the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface provides the [**IADs.Schema**](/windows/desktop/ADSI/iads-property-methods) property.</span></span> <span data-ttu-id="6fbc6-114">Questa proprietà restituisce ADsPath per la classe di oggetti nel formato della stringa di associazione dello schema astratto.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-114">This property returns the ADsPath for the object class in abstract schema binding string format.</span></span> <span data-ttu-id="6fbc6-115">Se si dispone di un puntatore **IADs** a un oggetto, è possibile eseguire l'associazione alla relativa classe nello schema astratto utilizzando ADsPath restituito da **IADs. Schema**.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-115">If you have an **IADs** pointer to an object, you can bind to its class in the abstract schema using the ADsPath returned from **IADs.Schema**.</span></span>

<span data-ttu-id="6fbc6-116">Per le classi, nella tabella seguente sono elencate le proprietà chiave fornite dallo schema astratto.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-116">For classes, the following table lists key properties provided by the abstract schema.</span></span>



| <span data-ttu-id="6fbc6-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6fbc6-117">Property</span></span>                                                             | <span data-ttu-id="6fbc6-118">Significato</span><span class="sxs-lookup"><span data-stu-id="6fbc6-118">Meaning</span></span>                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fbc6-119">**IADsClass. Abstract**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-119">**IADsClass.Abstract**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)            | <span data-ttu-id="6fbc6-120">Indica se si tratta di una classe astratta.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-120">Indicates whether this is an abstract class.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="6fbc6-121">**IADsClass. ausiliario**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-121">**IADsClass.Auxiliary**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="6fbc6-122">Indica se si tratta di una classe ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-122">Indicates whether this is an auxiliary class.</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="6fbc6-123">**IADsClass.AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-123">**IADsClass.AuxDerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)      | <span data-ttu-id="6fbc6-124">Matrice di classi ausiliarie da cui deriva questa classe.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-124">Array of auxiliary classes this class derives from.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="6fbc6-125">**IADsClass. container**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-125">**IADsClass.Container**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="6fbc6-126">Indica se gli oggetti di questa classe possono contenere altri oggetti, che è true se una classe include questa classe nell'elenco di **possibleSuperiors**.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-126">Indicates whether objects of this class can contain other objects, which is true if any class includes this class in its list of **possibleSuperiors**.</span></span>                                                                                                                                 |
| [<span data-ttu-id="6fbc6-127">**IADsClass. estratta da**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-127">**IADsClass.DerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)         | <span data-ttu-id="6fbc6-128">Matrice di classi da cui deriva questa classe.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-128">Array of classes that this class is derived from.</span></span>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="6fbc6-129">**IADsClass. MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-129">**IADsClass.MandatoryProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods) | <span data-ttu-id="6fbc6-130">Recupera una matrice delle proprietà obbligatorie che devono essere impostate per un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-130">Retrieves an array of the mandatory properties that must be set for an instance of the class.</span></span> <span data-ttu-id="6fbc6-131">L'elenco restituito include tutti i valori **mustContain** e **systemMustContain** per la classe e le classi da cui deriva, incluse le superclassi e le classi ausiliarie.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-131">The returned list includes all the **mustContain** and **systemMustContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span> |
| [<span data-ttu-id="6fbc6-132">**IADsClass. OID**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-132">**IADsClass.OID**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)                 | <span data-ttu-id="6fbc6-133">Recupera l'governsID della classe.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-133">Retrieves the governsID of the class.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="6fbc6-134">**IADsClass. OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-134">**IADsClass.OptionalProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)  | <span data-ttu-id="6fbc6-135">Recupera una matrice delle proprietà facoltative che possono essere impostate per un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-135">Retrieves an array of the optional properties that might be set for an instance of the class.</span></span> <span data-ttu-id="6fbc6-136">L'elenco restituito include tutti i valori **mayContain** e **systemMayContain** per la classe e le classi da cui deriva, incluse le superclassi e le classi ausiliarie.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-136">The returned list includes all the **mayContain** and **systemMayContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span>   |
| [<span data-ttu-id="6fbc6-137">**IADsClass. PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="6fbc6-137">**IADsClass.PossibleSuperiors**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)   | <span data-ttu-id="6fbc6-138">Recupera una matrice di valori **possibleSuperiors** per la classe, che indica le classi di oggetti che possono contenere oggetti di questa classe.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-138">Retrieves an array of the **possibleSuperiors** values for the class, which indicates the object classes that can contain objects of this class.</span></span>                                                                                                                                        |



 

<span data-ttu-id="6fbc6-139">Lo schema astratto viene archiviato nell'oggetto **sottoschema** del contenitore dello schema.</span><span class="sxs-lookup"><span data-stu-id="6fbc6-139">The abstract schema is stored in the **subSchema** object in the schema container.</span></span> <span data-ttu-id="6fbc6-140">Per ottenere il nome distinto dell'oggetto **sottoschema** , associare a RootDSE e leggere l'attributo **subschemaSubentry** , come descritto in [binding senza server e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="6fbc6-140">To get the distinguished name of the **subSchema** object, bind to rootDSE and read the **subSchemaSubEntry** attribute, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span> <span data-ttu-id="6fbc6-141">Tenere presente che è più efficiente leggere lo schema astratto mediante l'associazione a "LDAP://schema", rispetto al binding diretto all'oggetto **sottoschema** .</span><span class="sxs-lookup"><span data-stu-id="6fbc6-141">Be aware that it is more efficient to read the abstract schema by binding to "LDAP://schema", than by binding directly to the **subSchema** object.</span></span>

 

 