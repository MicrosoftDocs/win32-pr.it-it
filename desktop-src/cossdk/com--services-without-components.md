---
description: Servizi COM+ senza componenti
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Servizi COM+ senza componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127042"
---
# <a name="com-services-without-components"></a>Servizi COM+ senza componenti

Con COM+ 1,5, è possibile utilizzare i servizi forniti da COM+ senza che sia necessario compilare un componente che contenga i metodi che chiamano tali servizi. Si tratta di un vantaggio molto vantaggioso per gli sviluppatori che in genere non utilizzano componenti, ma che desiderano utilizzare servizi COM+ quali transazioni o lo strumento di rilevamento COM+. Utilizzando i servizi COM+ senza componenti, gli sviluppatori possono evitare il sovraccarico dovuto alla creazione di un componente utilizzato per accedere solo ai servizi COM+ necessari.

Gli ambienti di script, ad esempio, sono tradizionalmente gli utenti più grandi dei servizi COM+, ma non sono mai stati in grado di utilizzare i servizi in modo efficiente perché i servizi devono essere inclusi in un componente COM+. Questo requisito di aggregazione aumenta i costi di prestazioni a causa dell'aumento delle comunicazioni e della duplicazione dei dati necessari per l'interazione dell'ambiente di script con il componente. Usando i servizi senza componenti, questi costi sono ridotti al minimo.

Negli argomenti descritti nella tabella seguente vengono fornite informazioni di base e attività sull'utilizzo di servizi COM+ senza componenti. Questa funzionalità è destinata agli sviluppatori di Visual C++ avanzati che interessano le prestazioni.



| Argomento                                                                                                 | Descrizione                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Concetti relativi ai servizi COM+ senza componenti](com--services-without-components-concepts.md)<br/> | Viene fornita una panoramica dell'utilizzo dei servizi COM+ senza componenti.<br/>                     |
| [Servizi COM+ senza attività componenti](com--services-without-components-tasks.md)<br/>       | Vengono fornite istruzioni per l'utilizzo di COM+ per la creazione e l'utilizzo di servizi senza componenti.<br/> |



 

 

 




