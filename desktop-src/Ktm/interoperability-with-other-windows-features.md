---
description: Il Distributed Transaction Coordinator (DTC) consente transazioni distribuite o transazioni controllate da più gestori di risorse in uno o più sistemi. Per eseguire questa operazione, KTM e DTC interagiscono tra loro.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilità con altre funzionalità di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314306"
---
# <a name="interoperability-with-other-windows-features"></a>Interoperabilità con altre funzionalità di Windows

Il [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) consente *transazioni distribuite* o transazioni controllate da più gestori di risorse in uno o più sistemi. Per eseguire questa operazione, KTM e DTC interagiscono tra loro.

COM+ espone un modello dichiarativo per la programmazione transazionale. In altre parole, il programmatore dichiara la misura in cui un oggetto può sfruttare le transazioni e il runtime COM+ gestisce le transazioni per conto dell'oggetto. Un oggetto, ad esempio, può essere dichiarato per partecipare a una transazione solo se ne esiste già uno, per richiedere una transazione (ne viene creato uno se non esiste già), per richiedere una nuova transazione (uno viene creato indipendentemente dal fatto che ne esista già uno) oppure non è transazionale. Queste transazioni gestite in modo dichiarativo vengono utilizzate automaticamente per le connessioni al database create da oggetti COM+ che sono in esecuzione nel contesto di una transazione.

 

 
