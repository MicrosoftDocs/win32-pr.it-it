---
description: Un'estensione dello snap-in allegati deve consentire all'utente di modificare le informazioni di configurazione relative al servizio.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modifica delle informazioni di configurazione nell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6158d76d0f5114bd2d7b483e0af3d00f8f2439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316632"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modifica delle informazioni di configurazione nell'interfaccia utente

Un'estensione dello snap-in allegati deve consentire all'utente di modificare le informazioni di configurazione relative al servizio. Le informazioni modificate devono essere archiviate dall'estensione dello snap-in allegati fino a quando lo snap-in Configurazione sicurezza non chiama i metodi dell'interfaccia [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) per recuperare le informazioni.

Per evitare perdite di memoria, liberare memoria allocata dall'estensione dello snap-in chiamando [**ISceSvcAttachmentPersistInfo:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



