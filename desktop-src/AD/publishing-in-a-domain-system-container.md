---
title: Pubblicazione in un contenitore di sistema di dominio
description: Il contenitore di sistema di una partizione di dominio include informazioni operative per dominio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Pubblicazione in un dominio di Active Directory del contenitore di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855390"
---
# <a name="publishing-in-a-domain-system-container"></a>Pubblicazione in un contenitore di sistema di dominio

Il contenitore di sistema di una partizione di dominio include informazioni operative per dominio. Sono inclusi i criteri di sicurezza locali predefiniti, il rilevamento dei collegamenti di file, le riunioni di rete e i contenitori per i punti di connessione RpcNs (registrazione e risoluzione) di Windows Sockets (RnR) e del servizio nome RPC. Il contenitore di sistema è nascosto, per impostazione predefinita, e rappresenta una comoda posizione per archiviare gli oggetti di interesse per gli amministratori, ma non per gli utenti finali.

I servizi non collegati a un singolo host possono voler creare i convergenza nel contenitore di sistema di una partizione di dominio. Questa alternativa può essere utile per i servizi con repliche installate in più host, ogni replica che fornisce servizi identici ai client di tutto il dominio. Consente di raggruppare tutti gli oggetti per il servizio replicato in un singolo contenitore.

I servizi che creano oggetti specifici del servizio nel contenitore di sistema devono eseguire le operazioni seguenti:

1.  Creare un sottocontenitore del **contenitore** della classe di oggetti come elemento figlio immediato del contenitore di sistema. Assegnare a questo sottocontenitore un nome che lo identifichi chiaramente come pertinente per il servizio.
2.  Creare gli oggetti correlati al servizio in questo sottocontenitore. Ad esempio, NetMeeting usa il contenitore meetings per pubblicare gli oggetti della riunione di rete.

Un fornitore con più prodotti può utilizzare una strategia simile per raggruppare gli oggetti correlati ai servizi per tutti i prodotti. In questo caso, è possibile creare un oggetto **contenitore** con un nome che identifichi chiaramente il fornitore; quindi creare oggetti **contenitore** per ogni servizio come elementi figlio del contenitore Fornitore. Creare il contenitore specifico del fornitore come figlio del contenitore di sistema.

 

 




