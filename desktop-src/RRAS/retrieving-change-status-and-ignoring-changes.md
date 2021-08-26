---
title: Recupero dello stato delle modifiche e ignorare le modifiche
description: Il client può eseguire una query sul gestore delle tabelle di routing per scoprire se una notifica di una modifica a una destinazione è in sospeso chiamando RtmGetChangeStatus. Questa funzione restituisce TRUE finché il chiamante non recupera questa modifica chiamando RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a117130ac939788a74aaa32092000e8f6f29aa6b34e697ca6066c9e13259b8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028061"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Recupero dello stato delle modifiche e ignorare le modifiche

Il client può eseguire una query sul gestore delle tabelle di routing per verificare se una notifica di una modifica a una destinazione è in sospeso chiamando [**RtmGetChangeStatus.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus) Questa funzione restituisce **TRUE** finché il chiamante non recupera questa modifica chiamando [**RtmGetChangedDests.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)

Un client può usare questa query per evitare di eseguire un'azione che deve essere annullata dopo la ricezione e l'elaborazione della notifica di modifica. L'uso di questa funzionalità consente al client di funzionare in modo efficiente rinviando determinate operazioni a un momento successivo.

Il client può anche ignorare una notifica di modifica in sospeso per una destinazione chiamando [**RtmIgnoreChangedDests.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests) Una chiamata successiva a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) non restituisce questa destinazione a meno che non si verifichi un'altra modifica dopo la chiamata a [**RtmIgnoreChangedDests.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)

 

 




