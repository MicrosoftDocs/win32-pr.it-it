---
title: Sequenza di connessione
description: Illustrazione che mostra le chiamate al metodo effettuate tra il servizio Servizi Desktop remoto e il protocollo durante la sequenza di connessione del client.
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fe18d1a3b305a99fb0aaa35c51696f66de5c09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396678"
---
# <a name="connection-sequence"></a>Sequenza di connessione

Nella figura seguente sono illustrate le chiamate al metodo effettuate tra il servizio Servizi Desktop remoto e il protocollo durante la sequenza di connessione del client. Le azioni illustrate di seguito seguono la [sequenza di avvio](start-sequence.md). L'interazione tra il servizio e l'oggetto [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) rappresenta l'handshake delle licenze per il client.

![sequenza di connessione client](images/protocol-connectionsequence.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate al metodo](method-call-sequence.md)
</dt> <dt>

[Riconnetti sequenza](reconnect-sequence.md)
</dt> <dt>

[Sequenza di avvio](start-sequence.md)
</dt> </dl>

 

 




