---
title: Pubblicazione in un contenitore del sistema di dominio
description: Il contenitore System di una partizione di dominio contiene informazioni operative per dominio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Pubblicazione in un contenitore del sistema di dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb86a49bb14bc88d64a723ca9ab289723ff4ac2b9259f112323e19a04497362c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184955"
---
# <a name="publishing-in-a-domain-system-container"></a>Pubblicazione in un contenitore del sistema di dominio

Il contenitore System di una partizione di dominio contiene informazioni operative per dominio. Sono inclusi i criteri di sicurezza locali predefiniti, il rilevamento dei collegamenti file, le riunioni di rete e i contenitori per i punti di connessione RnR (Windows Sockets Registration and Resolution) e RPC Name Service (RpcNs). Il contenitore di sistema è nascosto, per impostazione predefinita, e offre una comoda posizione per l'archiviazione di oggetti di interesse per gli amministratori, ma non per gli utenti finali.

I servizi non associati a un singolo host possono voler creare i relativi scp nel contenitore System di una partizione di dominio. Questa alternativa può essere utile per i servizi con repliche installate in più host, ognuna delle quali fornisce servizi identici ai client in tutto il dominio. Consente di raggruppare tutti gli oggetti per il servizio replicato in un singolo contenitore.

I servizi che creano oggetti specifici del servizio nel contenitore System devono eseguire le operazioni seguenti:

1.  Creare un contenitore secondario del contenitore della classe **di** oggetti come figlio immediato del contenitore System. Assegnare a questo contenitore secondario un nome che lo identifichi chiaramente come relativo al servizio.
2.  Creare gli oggetti correlati al servizio in questo contenitore secondario. Ad esempio, NetMeeting usa il contenitore Riunioni per pubblicare oggetti riunione di rete.

Un fornitore con più prodotti può usare una strategia simile agli oggetti correlati ai servizi di gruppo per tutti i prodotti. In questo caso, è possibile creare un oggetto **contenitore** con un nome che identifica chiaramente il fornitore. quindi creare **oggetti contenitore** per ogni servizio come elementi figlio del contenitore del fornitore. Creare il contenitore specifico del fornitore come figlio del contenitore System.

 

 




