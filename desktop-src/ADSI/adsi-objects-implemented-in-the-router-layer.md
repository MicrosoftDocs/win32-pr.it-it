---
title: Oggetti ADSI implementati nel livello router
description: Nella tabella seguente viene illustrata una breve descrizione degli oggetti COM implementati nel router ADSI.
ms.assetid: bd446e05-a15d-4354-9204-1df4e360497c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fad496bbfea220dca0046cac40daf41120675
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395306"
---
# <a name="adsi-objects-implemented-in-the-router-layer"></a>Oggetti ADSI implementati nel livello router

Nella tabella seguente viene illustrata una breve descrizione degli oggetti COM implementati nel router ADSI.



| ADSI (oggetto)            | Descrizione                                                         | Interfacce supportate                                                                                                                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AccessControlEntry** | Oggetto ADSI che rappresenta una voce di controllo di accesso (ACE).       | [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)                                                                                                                                                                                                                                  |
| **AccessControlList**  | Oggetto ADSI che rappresenta un elenco di controllo di accesso (ACL).        | [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                                                                                                                                                                                                                                    |
| **ADsNamespaces**      | Oggetto ADSI che rappresenta il contenitore di vari spazi dei nomi. | <dl> <dt>[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)</dt> <dt>[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)</dt> <dt>[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)</dt> </dl> |
| **LargeInteger**       | Oggetto ADSI che rappresenta un numero intero grande.                     | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                                                                                                                                                                                                                                              |
| **Elemento PropertyEntry**      | Oggetto ADSI che rappresenta una voce della proprietà.                    | [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                                                                                                                                                                                                                                            |
| **PropertyValue**      | Oggetto ADSI che rappresenta un valore della proprietà.                    | [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                                                                                                                                                                                                                                            |
| **PropertyValue2**     | Oggetto ADSI che rappresenta un valore della proprietà.                    | [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)                                                                                                                                                                                                                                          |
| **SecurityDescriptor** | Oggetto ADSI che rappresenta un descrittore di sicurezza.               | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                                                                                                                                                                                                                  |



 

 

 




