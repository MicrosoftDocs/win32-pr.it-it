---
title: Mapping del codice Visual Basic ADSI al codice C++
description: ADSI è costituito da più di 50 interfacce.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a924f403dcbdbe89b1b0bbf846c95223b401a04d1925ce9362a5300faf828fe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179208"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>Mapping del codice Visual Basic ADSI al codice C++

ADSI è costituito da più di 50 interfacce. La maggior parte delle operazioni di directory può essere completata usando solo cinque interfacce. ovvero:

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IAD**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Nella tabella seguente sono elencati i mapping dal codice ADSI VB/VBS al codice C++. Tenere presente che non si tratta di un elenco completo.



| Codice VBS                           | Codice VC                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Impostare obj = GetObject()              | hr = AdsGetObject()                                                   |
| Obj. Inserire obj. Ottenere obj. genitore         | IAD o IDirectoryObject                                              |
| Obj. Creare obj. Eliminare obj. MoveHere | IADsContainer                                                         |
| Per ogni... Pollici...                      | AdsBuildEnumerator() ADsEnumerateNext()                               |
| Connection, Command, RecordSet     | IDirectorySearch                                                      |
| Descrittore di sicurezza, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




