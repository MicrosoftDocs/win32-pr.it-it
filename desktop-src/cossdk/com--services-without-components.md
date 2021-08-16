---
description: Servizi COM+ senza componenti
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Servizi COM+ senza componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b395186875c37fb42e5011ee0486aa6de86ffe62b73c8ea1a54c09e82a27c588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638451"
---
# <a name="com-services-without-components"></a>Servizi COM+ senza componenti

Con COM+ 1.5 è possibile usare i servizi forniti da COM+ senza dover compilare un componente per contenere i metodi che chiamano tali servizi. Ciò è molto vantaggioso per gli sviluppatori che in genere non usano componenti, ma vogliono usare i servizi COM+, ad esempio le transazioni o il tracker COM+. Usando i servizi COM+ senza componenti, gli sviluppatori possono evitare il sovraccarico della creazione di un componente usato per accedere solo ai servizi COM+ necessari.

Ad esempio, gli ambienti script sono stati tradizionalmente i più grandi consumer dei servizi COM+, ma non sono mai stati in grado di usare questi servizi in modo efficiente perché i servizi dovevano essere aggregati all'interno di un componente COM+. Questo requisito di raggruppamento ha aumentato i costi delle prestazioni a causa dell'aumento delle comunicazioni e della duplicazione dei dati necessari per l'interazione dell'ambiente di scripting con il componente. Usando i servizi senza componenti, tali costi vengono ridotti al minimo.

Gli argomenti descritti nella tabella seguente forniscono informazioni di base e attività sull'uso dei servizi COM+ senza componenti. Questa funzionalità è destinata agli sviluppatori Visual C++ esperti che si preoccupano delle prestazioni.



| Argomento                                                                                                 | Descrizione                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Concetti relativi ai servizi COM+ senza componenti](com--services-without-components-concepts.md)<br/> | Fornisce una panoramica dell'uso dei servizi COM+ senza componenti.<br/>                     |
| [Attività servizi COM+ senza componenti](com--services-without-components-tasks.md)<br/>       | Vengono fornite istruzioni per l'uso di COM+ per creare e usare servizi senza componenti.<br/> |



 

 

 




