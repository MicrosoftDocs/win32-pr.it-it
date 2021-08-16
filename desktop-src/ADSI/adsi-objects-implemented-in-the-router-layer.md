---
title: Oggetti ADSI implementati nel livello router
description: Nella tabella seguente viene presentata una breve descrizione degli oggetti COM implementati nel router ADSI.
ms.assetid: bd446e05-a15d-4354-9204-1df4e360497c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cc96eac8a2d680cb83622e01d94f8ef7a1d236726ab6b6fef9b2e6c5c40f50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692818"
---
# <a name="adsi-objects-implemented-in-the-router-layer"></a>Oggetti ADSI implementati nel livello router

Nella tabella seguente viene presentata una breve descrizione degli oggetti COM implementati nel router ADSI.



| Oggetto ADSI            | Descrizione                                                         | Interfacce supportate                                                                                                                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Accesscontrolentry** | Oggetto ADSI che rappresenta una voce di controllo di accesso (ACE).       | [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)                                                                                                                                                                                                                                  |
| **AccessControlList**  | Oggetto ADSI che rappresenta un elenco di controllo di accesso (ACL).        | [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                                                                                                                                                                                                                                    |
| **ADsNamespaces**      | Oggetto ADSI che rappresenta il contenitore di vari spazi dei nomi. | <dl> <dt>[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)</dt> <dt>[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)</dt> <dt>[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)</dt> </dl> |
| **LargeInteger**       | Oggetto ADSI che rappresenta un numero intero grande.                     | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                                                                                                                                                                                                                                              |
| **Propertyentry**      | Oggetto ADSI che rappresenta una voce di proprietà.                    | [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                                                                                                                                                                                                                                            |
| **PropertyValue**      | Oggetto ADSI che rappresenta il valore di una proprietà.                    | [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                                                                                                                                                                                                                                            |
| **PropertyValue2**     | Oggetto ADSI che rappresenta il valore di una proprietà.                    | [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)                                                                                                                                                                                                                                          |
| **SecurityDescriptor** | Oggetto ADSI che rappresenta un descrittore di sicurezza.               | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                                                                                                                                                                                                                  |



 

 

 




