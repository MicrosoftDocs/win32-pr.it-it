---
title: Mapping del codice Visual Basic ADSI al codice C++
description: ADSI è costituito da più di 50 interfacce.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297666"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>Mapping del codice Visual Basic ADSI al codice C++

ADSI è costituito da più di 50 interfacce. La maggior parte delle operazioni di directory può essere completata solo con cinque interfacce. Ad esempio:

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

La tabella seguente elenca i mapping dal codice ADSI VB/VBS al codice C++. Tenere presente che non si tratta di un elenco completo.



| Codice VBS                           | Codice VC                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject ()              | HR = AdsGetObject ()                                                   |
| obj. Inserire obj. Ottiene obj. Padre         | IADs o IDirectoryObject                                              |
| obj. Creazione di obj. Elimina obj. MoveHere | IADsContainer                                                         |
| Per ogni... in...                      | AdsBuildEnumerator() ADsEnumerateNext()                               |
| Connessione, comando, RecordSet     | IDirectorySearch                                                      |
| Descrittore di sicurezza, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




