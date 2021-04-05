---
description: I monitoraggi ricevono i frame di rete acquisiti in modalità in tempo reale. I frame vengono acquisiti da un provider di pacchetti di rete (NPP) utilizzando l'interfaccia COM Providers IRTC e passati al monitoraggio in uno dei monitoraggi due thread di esecuzione.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Acquisizioni di Real-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885677"
---
# <a name="real-time-captures"></a>Acquisizioni di Real-Time

I monitoraggi ricevono i frame di rete acquisiti in modalità in tempo reale. I frame vengono acquisiti da un [*provider di pacchetti di rete*](n.md) (NPP) utilizzando l'interfaccia com [IRTC](irtc.md) del provider e passati al monitoraggio in uno dei due thread di esecuzione del monitoraggio.

I monitoraggi possono limitare il numero di frame da elaborare passando un filtro di [*acquisizione*](c.md) all'oggetto NPP che fornisce i frame. In genere, un monitoraggio specifico è progettato per controllare i tipi di traffico specifici, ad esempio HTTP, RIPX o SMB. Diversamente dagli esperti, che usano parser sofisticati per selezionare le informazioni da analizzare, un monitoraggio deve esaminare ogni frame per le condizioni che è stato progettato per rilevare. Il motivo alla base di questo approccio frame per fotogramma è la prestazione. Un monitoraggio deve elaborare i frame in modo sufficientemente rapido, in modo che non si trovino dietro il driver che fornisce i frame all'oggetto NPP. In caso contrario, i dati andranno perduti.

 

 



