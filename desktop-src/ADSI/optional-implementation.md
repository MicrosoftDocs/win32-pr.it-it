---
title: Implementazione facoltativa
description: Le funzionalità seguenti sono facoltative, ma consigliate
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Implementazione facoltativa di ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515457"
---
# <a name="optional-implementation"></a>Implementazione facoltativa

Le funzionalità seguenti sono facoltative, ma consigliate:

-   Interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per client non di automazione. Poiché il provider di OLE DB ADSI utilizza **IDirectorySearch** per presentare le query e raccogliere i risultati dal servizio directory sottostante, i provider che implementano questa interfaccia forniscono automaticamente l'accesso ai database di OLE DB Style senza implementare interfacce aggiuntive.
-   Interfacce [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) . I provider per i servizi directory che supportano la sicurezza degli oggetti basata su ACL sono invitati a implementare queste funzionalità aggiuntive.

 

 




