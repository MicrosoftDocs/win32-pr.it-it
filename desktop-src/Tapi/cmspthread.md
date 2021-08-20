---
description: La classe CMSPThread implementa il thread di lavoro MSPs.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992efdc7f46772ee7766ba38ebab4cf3a9adc502e7c4001eb91779d03c677d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946677"
---
# <a name="cmspthread"></a>CMSPThread

La **classe CMSPThread** implementa il thread di lavoro di MSP. Le classi di base usano questo thread di lavoro per diversi scopi. Viene fornito un meccanismo di elemento di lavoro generico e leggero per consentire al msp derivato di usare questo thread per i propri elementi di lavoro sincroni o asincroni, indipendentemente dal fatto che siano. Il thread esegue anche il pump dei messaggi e supporta la gestione delle API (anche se le API non vengono usate nelle classi di base).

Quando sono presenti più indirizzi simili, ovvero quando viene creata più volte un'istanza della stessa implementazione MSP della stessa DLL, la classe thread garantisce la scalabilità usando automaticamente un singolo thread per tutti gli indirizzi. L'interfaccia alla classe di thread è tale che l'implementazione di MSP può pensare alla classe di thread come a un thread privato e non deve occuparsi degli altri indirizzi che potrebbero condividerla.

Definito in MSPthrd.h.

 

 



