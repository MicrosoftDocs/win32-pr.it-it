---
title: Enumerazione di entità registrate
description: Dopo la registrazione di un client, il client può ottenere un elenco di tutti gli altri client registrati con gestione tabelle di routing. Alcuni client devono eseguire determinate operazioni se viene rilevata la presenza di un particolare tipo di client.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d67a810806c1bc29f8f18c4cdea9f3a36e5b5a95922e8f66a943a99923ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674161"
---
# <a name="enumerating-registered-entities"></a>Enumerazione di entità registrate

Dopo la registrazione di un client, il client può ottenere un elenco di tutti gli altri client registrati con gestione tabelle di routing. Alcuni client devono eseguire determinate operazioni se viene rilevata la presenza di un particolare tipo di client.

Il client può chiamare la [**funzione RtmGetRegisteredEntities.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) Viene restituito un buffer di strutture [**\_ ENTITY \_ INFO RTM.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) Dopo che il client ha elaborato queste informazioni, il client deve chiamare [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) per rilasciare gli handle nelle strutture **\_ RTM ENTITY \_ INFO.**

Se il client di gestione tabelle di routing ha fornito una funzione di callback nella chiamata a [**RtmRegisterEntity,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)il client viene informato quando altri client registrano o annullano la registrazione.

Per il codice di esempio che illustra come usare queste funzioni, vedere [Enumerare le](enumerate-the-registered-entities.md) entità registrate e [Usare il callback di notifica degli eventi](use-the-event-notification-callback.md).

 

 




