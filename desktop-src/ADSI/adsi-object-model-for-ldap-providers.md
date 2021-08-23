---
title: Modello a oggetti ADSI per provider LDAP
description: Figura che mostra gli oggetti ADSI utilizzati per il provider LDAP e le interfacce utilizzate per accedere a tali oggetti.
ms.assetid: 109fd42e-201e-4b84-a213-2695d81f005b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c7c520793f6095bc9d4d9c6379f8ff6f09766f39ae6102f7e0a82d3a3de7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023794"
---
# <a name="adsi-object-model-for-ldap-providers"></a>Modello a oggetti ADSI per provider LDAP

Nella figura seguente vengono illustrati gli oggetti ADSI utilizzati per il provider LDAP e le interfacce utilizzate per accedere a tali oggetti.

![modello a oggetti per il provider LDAP](images/adsiobjmodldap-gif-1.png)

| Oggetto                        | Interfaccia                                                                                                                                                                                                                                                                                      |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Classe<br/>              | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                                                                                                                                                                                                                           |
| Proprietà<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                                                                                                                                                                                                                                     |
| Oggetto GenObject<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops), [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) |
| Spazio dei nomi<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                                                                                                                                                                                     |
| Rootdse<br/>            | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                                                                                                                                                                                                                             |
| Percorso<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)                                                                                                                                                                                                                                     |
| Schema<br/>             | [**IAD**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                                                                                                                                                                                                                                   |
| Sintassi<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                                                                                                                                                                                                                                         |
| Organization<br/>       | [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                                                                                                                                                                                                                                                         |
| OrganizationalUnit<br/> | [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                                                                                                                                                                                                                                                       |
| Groupcollection<br/>    | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Group<br/>              | [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                                                                                                                                                                                                                                                 |
| UserCollection<br/>     | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Utente<br/>               | [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                                                                                                                                                                                                                                                   |
| Località<br/>           | [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                                                                                                                                                                                                                                                           |
| NameTranslate<br/>      | [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)                                                                                                                                                                                                                                                 |
| PrintQueue<br/>         | [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue), [ **IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)                                                                                                                                                                                         |



 

 

 





