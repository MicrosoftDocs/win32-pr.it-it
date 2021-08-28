---
description: Un'estensione dello snap-in degli allegati deve consentire all'utente di modificare le informazioni di configurazione relative al servizio.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modifica delle informazioni di configurazione nel Interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 414e2ab1475ec1c3241d60b96d182a522c299a9f5cf6134f50339c2088c99d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005119"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modifica delle informazioni di configurazione nel Interfaccia utente

Un'estensione dello snap-in degli allegati deve consentire all'utente di modificare le informazioni di configurazione relative al servizio. Le informazioni modificate devono essere archiviate dall'estensione dello snap-in allegato fino a quando lo snap-in Configurazione sicurezza non chiama i metodi [**dell'interfaccia ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) per recuperare le informazioni.

Per evitare perdite di memoria, liberare la memoria allocata dall'estensione dello snap-in chiamando [**ISceSvcAttachmentPersistInfo::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



