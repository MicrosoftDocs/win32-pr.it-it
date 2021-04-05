---
title: Recupero dello stato delle modifiche e delle modifiche ignorate
description: Il client può eseguire una query su Gestione tabelle di routing per verificare se una notifica di una modifica a una destinazione è in sospeso chiamando RtmGetChangeStatus. Questa funzione restituisce TRUE finché il chiamante non recupera questa modifica chiamando RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709103"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Recupero dello stato delle modifiche e delle modifiche ignorate

Il client può eseguire una query su Gestione tabelle di routing per verificare se una notifica di una modifica a una destinazione è in sospeso chiamando [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus). Questa funzione restituisce **true** finché il chiamante non recupera questa modifica chiamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).

Un client può utilizzare questa query per evitare di eseguire un'azione che dovrebbe essere annullata dopo la ricezione e l'elaborazione della notifica di modifica. L'uso di questa funzionalità consente al client di lavorare in modo efficiente rinviando determinate operazioni a un momento successivo.

Il client può anche ignorare una notifica di modifica in sospeso per una destinazione chiamando [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests). Una chiamata successiva a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) non restituisce questa destinazione a meno che non si verifichi un'altra modifica dopo la chiamata a [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).

 

 




