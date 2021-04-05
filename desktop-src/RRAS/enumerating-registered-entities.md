---
title: Enumerazione delle entità registrate
description: Dopo la registrazione di un client, il client può ottenere un elenco di tutti gli altri client registrati con gestione tabelle di routing. Alcuni client devono eseguire determinate operazioni se viene rilevata la presenza di un determinato tipo di client.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044765"
---
# <a name="enumerating-registered-entities"></a>Enumerazione delle entità registrate

Dopo la registrazione di un client, il client può ottenere un elenco di tutti gli altri client registrati con gestione tabelle di routing. Alcuni client devono eseguire determinate operazioni se viene rilevata la presenza di un determinato tipo di client.

Il client può chiamare la funzione [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) . Viene restituito un buffer di strutture di [**\_ \_ informazioni sull'entità RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) . Dopo che il client ha elaborato queste informazioni, il client deve chiamare [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) per rilasciare gli handle nelle strutture delle **\_ \_ informazioni sull'entità RTM** .

Se il client di gestione tabelle di routing ha fornito una funzione di callback nella chiamata a [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), il client riceve una notifica quando viene effettuata la registrazione o l'annullamento della registrazione di altri client.

Per il codice di esempio che illustra come usare queste funzioni, vedere [enumerare le entità registrate](enumerate-the-registered-entities.md) e [usare il callback di notifica degli eventi](use-the-event-notification-callback.md).

 

 




