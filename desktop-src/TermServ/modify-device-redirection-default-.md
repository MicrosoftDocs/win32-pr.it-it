---
title: Modificare il reindirizzamento dei dispositivi predefinito
description: Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client a un server host sessione Desktop remoto, potrebbe essere necessario disabilitare questa impostazione predefinita in alcuni casi.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b74515f6bf79b42c129ec7c113729b9871d4e4bfb0101f845f91dcac0d49237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138171"
---
# <a name="modify-device-redirection-default"></a>Modificare il reindirizzamento dei dispositivi predefinito

Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client a un server host sessione Desktop remoto, potrebbe essere necessario disabilitare questa impostazione predefinita in alcuni casi.

In Windows Server 2008 R2 e versioni successive, i server gateway Desktop remoto tenteranno per impostazione predefinita di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client a un server host sessione Desktop remoto. Tuttavia, questa funzionalità non è supportata da alcuni server. Ad esempio, questa opzione non è supportata per le connessioni alle sessioni della console Hyper-V e potrebbe essere necessario disabilitare l'impostazione predefinita per supportare l'autenticazione federata. In questi casi, questa funzionalità può essere disabilitata creando la chiave del Registro di sistema seguente per consentire il passare attraverso le connessioni.

**HKEY \_ LOCAL MACHINE Software Microsoft Terminal Server Gateway \_ \\ \\ \\ \\ preRDPDisableRegKey**

Quando questa chiave esiste, il Desktop remoto gateway non imposirà il reindirizzamento dei dispositivi.

 

 




