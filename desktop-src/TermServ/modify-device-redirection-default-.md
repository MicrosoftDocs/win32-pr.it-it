---
title: Modificare il reindirizzamento dei dispositivi predefinito
description: Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client tramite a un server host sessione Desktop remoto, potrebbe essere necessario disabilitare questa impostazione predefinita in alcuni casi.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856293"
---
# <a name="modify-device-redirection-default"></a>Modificare il reindirizzamento dei dispositivi predefinito

Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client tramite a un server host sessione Desktop remoto, potrebbe essere necessario disabilitare questa impostazione predefinita in alcuni casi.

In Windows Server 2008 R2 e versioni successive, per impostazione predefinita Desktop remoto server gateway tenterà di applicare i criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client tramite a un server host sessione Desktop remoto. Questa funzionalità, tuttavia, non è supportata da alcuni server. Ad esempio, questa operazione non è supportata per le connessioni alle sessioni della console Hyper-V e potrebbe essere necessario disabilitare l'impostazione predefinita per supportare l'autenticazione federata. In questi casi, è possibile disabilitare questa funzionalità creando la seguente chiave del registro di sistema per consentire le connessioni.

**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ terminal server gateway \\ preRDPDisableRegKey**

Quando questa chiave esiste, il Gateway Desktop remoto non impone il reindirizzamento dei dispositivi.

 

 




