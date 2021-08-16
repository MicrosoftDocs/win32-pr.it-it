---
title: Implementazione facoltativa
description: Le funzionalità seguenti sono facoltative, ma consigliate
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Implementazione facoltativa di ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3074f3ef6b4d36713d483937ad0f6ef10167777a7c36f8d21427d7df2b0485a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838951"
---
# <a name="optional-implementation"></a>Implementazione facoltativa

Le funzionalità seguenti sono facoltative, ma consigliate:

-   Interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per i client non di automazione. Poiché il provider OLE DB ADSI usa **IDirectorySearch** per presentare le query e raccogliere i risultati dal servizio directory sottostante, i provider che implementano questa interfaccia forniscono automaticamente l'accesso ai database in stile OLE DB senza dover implementare interfacce aggiuntive.
-   Interfacce [**IADsSecurityDescriptor,**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry.**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) I provider per i servizi directory che supportano la sicurezza degli oggetti basata su ACL sono invitati a implementare queste funzionalità aggiuntive.

 

 




