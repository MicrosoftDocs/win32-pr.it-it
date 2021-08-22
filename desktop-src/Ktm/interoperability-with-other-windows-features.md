---
description: Il Distributed Transaction Coordinator (DTC) consente transazioni distribuite o transazioni sotto il controllo di più gestori di risorse in uno o più sistemi. KTM e DTC collaborano strettamente a questo scopo.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilità con altre Windows funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18595140676539c6e5acaa5fc62835ac279215d068834e3e56dffe50d01e0e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119265071"
---
# <a name="interoperability-with-other-windows-features"></a>Interoperabilità con altre Windows funzionalità

Il [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) abilita le transazioni distribuite *o* le transazioni sotto il controllo di più gestori di risorse in uno o più sistemi. KTM e DTC collaborano strettamente a questo scopo.

COM+ espone un modello dichiarativo per la programmazione transazionale. In altre parole, il programmatore dichiara la misura in cui un oggetto può sfruttare le transazioni e il runtime COM+ gestisce le transazioni per conto dell'oggetto. Ad esempio, un oggetto può essere dichiarato per partecipare a una transazione solo se ne esiste già una, per richiedere una transazione (se non esiste già), per richiedere una nuova transazione (ne viene creata una indipendentemente dal fatto che ne esista già una) o non è transazionale. Queste transazioni gestite in modo dichiarativo vengono usate automaticamente nelle connessioni di database create da oggetti COM+ in esecuzione nel contesto di una transazione.

 

 
