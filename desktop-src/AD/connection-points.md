---
title: Punti di connessione
description: Un oggetto punto di connessione contiene i dati relativi a una o più istanze di un servizio disponibili in rete.
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- Active Directory punti di connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc61c4c5b7dd74626ab1f3884ad403cfa20b843
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046545"
---
# <a name="connection-points"></a>Punti di connessione

Un oggetto punto di connessione contiene i dati relativi a una o più istanze di un servizio disponibili in rete. La classe di oggetti [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) è la classe di base astratta da cui derivano gli oggetti che rappresentano le risorse connettibili in Active Directory Domain Services. Nella figura seguente vengono illustrate alcune classi di oggetti derivate dalla classe di oggetti **ConnectionPoint** .

![classi di oggetti derivate dalla classe di oggetti ConnectionPoint](images/connection-points.png)

Nella tabella seguente sono elencate le sottoclassi immediate della classe [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) .



| Classe Object                                                    | Descrizione                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | Oggetti del punto di connessione del servizio (SCP) per la pubblicazione di dati usati dalle applicazioni client per l'associazione a un servizio. Per ulteriori informazioni, vedere [pubblicazione con i punti di connessione del servizio (convergenza)](publishing-with-service-connection-points.md).                                                                               |
| [**rpcEntry**](/windows/desktop/ADSchema/c-rpcentry)                             | Una classe astratta le cui sottoclassi vengono usate dal servizio del nome RPC (NS) a cui si accede tramite le funzioni **RpcNs \*** nell'API Win32. Per ulteriori informazioni, vedere [la pagina relativa alla pubblicazione con il servizio nome RPC (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md).                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | Oggetto punto di connessione utilizzato dal servizio Windows Sockets Registration and Resolution (RnR), a cui si accede tramite le API **WSA \*** di Windows Sockets. Per ulteriori informazioni, vedere la pagina relativa alla [pubblicazione con la registrazione e la risoluzione di Windows Sockets (RNR)](publishing-with-windows-sockets-registration-and-resolution.md). |
| [**printQueue**](/windows/desktop/ADSchema/c-printqueue)                         | Oggetto punto di connessione usato per pubblicare le stampanti di rete. Per ulteriori informazioni, vedere [**IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue).                                                                                                                                                                                           |
| [**volume**](/windows/desktop/ADSchema/c-volume)                                 | Oggetto punto di connessione utilizzato per pubblicare servizi file.                                                                                                                                                                                                                                                                   |



 

Tenere presente che i servizi basati su COM non utilizzano oggetti punto di connessione per annunciare se stessi. Questi servizi vengono pubblicati nell'archivio delle classi. L'archivio di classi di Windows 2000 è un repository basato su directory per tutte le applicazioni, le interfacce e le API basate su COM che consentono la pubblicazione e l'assegnazione di applicazioni. Per ulteriori informazioni, vedere [pubblicazione di servizi com+](publishing-com-services.md).

 

 