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
# <a name="reading-the-abstract-schema"></a>Lettura dello schema astratto

In questo argomento vengono forniti un esempio di codice e linee guida per la lettura dallo schema astratto, che fornisce un subset dei dati archiviati negli oggetti **attributeSchema** e **classSchema** nel contenitore dello schema. Per recuperare i dati non disponibili nello schema astratto, leggere i dati direttamente dal contenitore dello schema come descritto in [lettura degli oggetti attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).

Utilizzare la stringa di associazione "LDAP://schema" per eseguire il binding a un puntatore [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) nello schema astratto. Utilizzare questo puntatore per enumerare le voci relative a classi, attributi e sintassi nello schema astratto. È anche possibile usare il metodo [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) per recuperare singole voci.


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



Usare una stringa di associazione simile, "LDAP://schema/ <object> ", per eseguire l'associazione diretta a una voce di classe o attributo nello schema astratto. In questa stringa " &lt; Object &gt; " è l' **ldapDisplayName** di una classe o di un attributo. Per le classi sono associate all'interfaccia [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) ; per gli attributi, associare l'interfaccia [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) .


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



Inoltre, l'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) fornisce la proprietà [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) . Questa proprietà restituisce ADsPath per la classe di oggetti nel formato della stringa di associazione dello schema astratto. Se si dispone di un puntatore **IADs** a un oggetto, è possibile eseguire l'associazione alla relativa classe nello schema astratto utilizzando ADsPath restituito da **IADs. Schema**.

Per le classi, nella tabella seguente sono elencate le proprietà chiave fornite dallo schema astratto.



| Proprietà                                                             | Significato                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsClass. Abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Indica se si tratta di una classe astratta.                                                                                                                                                                                                                                            |
| [**IADsClass. ausiliario**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica se si tratta di una classe ausiliaria.                                                                                                                                                                                                                                           |
| [**IADsClass.AuxDerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | Matrice di classi ausiliarie da cui deriva questa classe.                                                                                                                                                                                                                                     |
| [**IADsClass. container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica se gli oggetti di questa classe possono contenere altri oggetti, che è true se una classe include questa classe nell'elenco di **possibleSuperiors**.                                                                                                                                 |
| [**IADsClass. estratta da**](/windows/desktop/ADSI/iadsclass-property-methods)         | Matrice di classi da cui deriva questa classe.                                                                                                                                                                                                                                       |
| [**IADsClass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) | Recupera una matrice delle proprietà obbligatorie che devono essere impostate per un'istanza della classe. L'elenco restituito include tutti i valori **mustContain** e **systemMustContain** per la classe e le classi da cui deriva, incluse le superclassi e le classi ausiliarie. |
| [**IADsClass. OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Recupera l'governsID della classe.                                                                                                                                                                                                                                                   |
| [**IADsClass. OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | Recupera una matrice delle proprietà facoltative che possono essere impostate per un'istanza della classe. L'elenco restituito include tutti i valori **mayContain** e **systemMayContain** per la classe e le classi da cui deriva, incluse le superclassi e le classi ausiliarie.   |
| [**IADsClass. PossibleSuperiors**](/windows/desktop/ADSI/iadsclass-property-methods)   | Recupera una matrice di valori **possibleSuperiors** per la classe, che indica le classi di oggetti che possono contenere oggetti di questa classe.                                                                                                                                        |



 

Lo schema astratto viene archiviato nell'oggetto **sottoschema** del contenitore dello schema. Per ottenere il nome distinto dell'oggetto **sottoschema** , associare a RootDSE e leggere l'attributo **subschemaSubentry** , come descritto in [binding senza server e RootDSE](serverless-binding-and-rootdse.md). Tenere presente che è più efficiente leggere lo schema astratto mediante l'associazione a "LDAP://schema", rispetto al binding diretto all'oggetto **sottoschema** .

 

 