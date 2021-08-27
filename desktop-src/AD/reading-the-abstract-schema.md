---
title: Lettura dello schema astratto
description: Questo argomento fornisce un esempio di codice e linee guida per la lettura dallo schema astratto, che fornisce un subset dei dati archiviati negli oggetti attributeSchema e classSchema nel contenitore dello schema.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- schema Active Directory , lettura dello schema astratto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7095dc4fb5ffe5f11f64781ecd423a60b3d434d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881311"
---
# <a name="reading-the-abstract-schema"></a>Lettura dello schema astratto

Questo argomento fornisce un esempio di codice e linee guida per la lettura dallo schema astratto, che fornisce un subset dei dati archiviati negli oggetti **attributeSchema** e **classSchema** nel contenitore dello schema. Per recuperare i dati non disponibili nello schema astratto, leggere i dati direttamente dal contenitore dello schema, come descritto in [Lettura di attributeSchema e classSchema Objects](reading-attributeschema-and-classschema-objects.md).

Usare la stringa di associazione "LDAP://schema" per eseguire l'associazione a un [**puntatore IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) nello schema astratto. Usare questo puntatore per enumerare le voci di classe, attributo e sintassi nello schema astratto. È anche possibile usare il [**metodo IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) per recuperare singole voci.


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



Usare una stringa di associazione simile, "LDAP://schema/ object", per eseguire l'associazione direttamente a una classe o a una voce &lt; di attributo nello schema &gt; astratto. In questa stringa " &lt; object &gt; " è **lDAPDisplayName** di una classe o di un attributo. Per le classi associabili [**all'interfaccia IADsClass;**](/windows/desktop/api/iads/nn-iads-iadsclass) per gli attributi, associare [**all'interfaccia IADsProperty.**](/windows/desktop/api/iads/nn-iads-iadsproperty)


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



Inoltre, [**l'interfaccia IADs**](/windows/desktop/api/iads/nn-iads-iads) fornisce la [**proprietà IADs.Schema.**](/windows/desktop/ADSI/iads-property-methods) Questa proprietà restituisce ADsPath per la classe di oggetti in formato stringa di associazione dello schema astratto. Se si dispone di **un puntatore IADs** a un oggetto, è possibile eseguire l'associazione alla relativa classe nello schema astratto usando l'oggetto ADsPath restituito da **IADs.Schema**.

Per le classi, nella tabella seguente sono elencate le proprietà chiave fornite dallo schema astratto.



| Proprietà                                                             | Significato                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsClass.Abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Indica se si tratta di una classe astratta.                                                                                                                                                                                                                                            |
| [**IADsClass.Auxiliary**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica se si tratta di una classe ausiliaria.                                                                                                                                                                                                                                           |
| [**IADsClass.AuxDerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | Matrice di classi ausiliarie da cui deriva questa classe.                                                                                                                                                                                                                                     |
| [**IADsClass.Container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica se gli oggetti di questa classe possono contenere altri oggetti, vale a dire se una classe include questa classe nel relativo elenco di **possibiliSuperiors.**                                                                                                                                 |
| [**IADsClass.DerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)         | Matrice di classi da cui deriva questa classe.                                                                                                                                                                                                                                       |
| [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) | Recupera una matrice delle proprietà obbligatorie che devono essere impostate per un'istanza della classe . L'elenco restituito include tutti i valori **mustContain** e **systemMustContain** per la classe e le classi da cui deriva, incluse le superclassi e le classi ausiliarie. |
| [**IADsClass.OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Recupera il governsID della classe.                                                                                                                                                                                                                                                   |
| [**IADsClass.OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | Recupera una matrice delle proprietà facoltative che possono essere impostate per un'istanza della classe . L'elenco restituito include tutti i valori **mayContain** e **systemMayContain** per la classe e le classi da cui deriva, incluse le superclassi e le classi ausiliarie.   |
| [**IADsClass.PossibleSuperiors**](/windows/desktop/ADSI/iadsclass-property-methods)   | Recupera una matrice dei **valori possibleSuperiors** per la classe , che indica le classi di oggetti che possono contenere oggetti di questa classe.                                                                                                                                        |



 

Lo schema astratto viene archiviato **nell'oggetto subSchema** nel contenitore dello schema. Per ottenere il nome distinto dell'oggetto **subSchema,** eseguire il binding a rootDSE e leggere l'attributo **subSchemaSubEntry,** come descritto in [Associazione serverless e RootDSE](serverless-binding-and-rootdse.md). Tenere presente che è più efficiente leggere lo schema astratto tramite l'associazione a "LDAP://schema", che tramite l'associazione direttamente **all'oggetto subSchema.**

 

 
