---
description: Per gestire i record, è possibile usare le informazioni archiviate nelle strutture PEER \_ RECORD.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Gestione record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a747ae16e1773fe5944f2e9afdde8377d5e100a9a91316f70bcd1be8db6cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011519"
---
# <a name="record-management"></a>Gestione record

Per gestire i record, è possibile usare le informazioni archiviate nelle [**strutture PEER \_ RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record) Quando i record vengono creati, aggiornati o eliminati, le modifiche apportate a un grafo vengono replicate in tutti i nodi. La tabella seguente identifica le regole per l'aggiornamento e l'aggiornamento automatico dei record.



| Attività di gestione     | Regola                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aggiornamento di un record   | Mantenere la stessa ora di scadenza o aumentarla. Non è possibile ridurre l'ora di scadenza.                                                                                                                      |
| Aggiornamento di un record | Usare il flag [**PEER \_ RECORD FLAG \_ \_ AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) per aggiornare automaticamente un record. Usare questo flag solo quando il nodo che pubblica un record è online. In caso contrario, non usare questo flag. |



 

 

 



