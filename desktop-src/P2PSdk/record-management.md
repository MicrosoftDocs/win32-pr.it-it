---
description: Per gestire i record, è possibile utilizzare le informazioni archiviate in \_ strutture di record peer.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gestione dei record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314739"
---
# <a name="record-management"></a>Gestione dei record

Per gestire i record, è possibile utilizzare le informazioni archiviate in strutture di [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Quando i record vengono creati, aggiornati o eliminati, le modifiche apportate a un grafo vengono replicate in tutti i nodi. Nella tabella seguente vengono identificate le regole per l'aggiornamento e l'aggiornamento automatico dei record.



| Attività di gestione     | Regola                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aggiornamento di un record   | Mantenerne lo stesso tempo o aumentarlo. Non è possibile ridurre l'ora di scadenza.                                                                                                                      |
| Aggiornamento di un record | Usare il flag di aggiornamento automatico del [**\_ flag di record \_ \_ peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) per aggiornare automaticamente un record. Utilizzare questo flag solo quando il nodo che pubblica un record è online. In caso contrario, non usare questo flag. |



 

 

 



