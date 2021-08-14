---
title: Punti di connessione
description: Un oggetto punto di connessione contiene dati relativi a una o più istanze di un servizio disponibili nella rete.
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- punti di connessione ad Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0b7a4c8ddbf592bba0ed39e2eb8f93faf863e6ebff7081865466b6522c98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022047"
---
# <a name="connection-points"></a>Punti di connessione

Un oggetto punto di connessione contiene dati relativi a una o più istanze di un servizio disponibili nella rete. La [**classe di oggetti connectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) è la classe base astratta da cui derivano gli oggetti che rappresentano le risorse Active Directory Domain Services connessione. Nella figura seguente vengono illustrate alcune delle classi di oggetti derivate dalla **classe di oggetti connectionPoint.**

![Classi di oggetti derivate dalla classe dell'oggetto punto di connessione](images/connection-points.png)

Nella tabella seguente sono elencate le sottoclassi immediate della [**classe connectionPoint.**](/windows/desktop/ADSchema/c-connectionpoint)



| Classe Object                                                    | Descrizione                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | Oggetti punto di connessione del servizio (SCP) per la pubblicazione di dati utilizzati dalle applicazioni client per l'associazione a un servizio. Per altre informazioni, vedere [Pubblicazione con punti di connessione del servizio .](publishing-with-service-connection-points.md)                                                                               |
| [**rpcEntry**](/windows/desktop/ADSchema/c-rpcentry)                             | Classe astratta le cui sottoclassi vengono usate dal servizio NS (RPC Name Service) a cui si accede tramite le funzioni **RpcNs \*** nell'API Win32. Per altre informazioni, vedere [Pubblicazione con RPC Name Service (RpcNs).](publishing-with-the-rpc-name-service-rpcns.md)                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | Oggetto punto di connessione usato dal servizio dei nomi RnR (Windows Sockets Registration and Resolution), accessibile tramite le API **WSA \*** Windows Sockets. Per altre informazioni, vedere [Publishing with Windows Sockets Registration and Resolution (RnR) (Pubblicazione](publishing-with-windows-sockets-registration-and-resolution.md)con la registrazione e la risoluzione dei socket di rete ). |
| [**Printqueue**](/windows/desktop/ADSchema/c-printqueue)                         | Oggetto punto di connessione utilizzato per pubblicare stampanti di rete. Per altre informazioni, vedere [**IADsPrintQueue.**](/windows/desktop/api/iads/nn-iads-iadsprintqueue)                                                                                                                                                                                           |
| [**Volume**](/windows/desktop/ADSchema/c-volume)                                 | Oggetto punto di connessione utilizzato per pubblicare servizi file.                                                                                                                                                                                                                                                                   |



 

Tenere presente che i servizi basati su COM non usano oggetti punto di connessione per annunciarsi. Questi servizi vengono pubblicati nell'archivio classi. L Windows 2000 è un repository basato su directory per tutte le applicazioni, le interfacce e le API basate su COM che consentono la pubblicazione e l'assegnazione di applicazioni. Per altre informazioni, vedere [Pubblicazione di servizi COM+.](publishing-com-services.md)

 

 