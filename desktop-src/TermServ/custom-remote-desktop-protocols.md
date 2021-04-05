---
title: API del provider Remote Desktop Protocol
description: Usare l'API del provider Remote Desktop Protocol per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955059"
---
# <a name="remote-desktop-protocol-provider-api"></a>API del provider Remote Desktop Protocol

Usare l'API del provider Remote Desktop Protocol per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.

Quando si carica Windows Server, viene avviato il servizio di Servizi Desktop remoto (noto anche come gestione connessione remota (RCM)). Il servizio avvia anche gli oggetti listener per i provider di Remote Desktop Protocol che a loro volta restano in ascolto delle connessioni client. Il servizio e i provider di protocollo sono oggetti in modalità utente che comunicano usando le API descritte in questa documentazione. I provider di protocollo possono comunicare con i driver in modalità kernel utilizzando i controlli di input/output (IOCTL). Questo aspetto è illustrato nella figura seguente.

![architettura API del protocollo personalizzato](images/protocol-architecture.png)

Microsoft ha implementato il Remote Desktop Protocol (RDP) per fornire la comunicazione tra il servizio di Servizi Desktop remoto e le connessioni client. È possibile creare un protocollo personalizzato utilizzando interfacce, strutture, unioni e tipi di enumerazione che costituiscono l'API del provider Remote Desktop Protocol. Per ulteriori informazioni, vedere gli argomenti seguenti.

<dl> <dt>

[Creazione di un provider di Remote Desktop Protocol](creating-a-custom-remote-protocol.md)
</dt> <dd>

Informazioni sulla creazione di un provider di Remote Desktop Protocol. Gestione protocolli viene implementato come server COM e registrato in un percorso in cui viene eseguita la ricerca all'avvio del servizio Servizi Desktop remoto.

</dd> <dt>

[Riferimento al provider Remote Desktop Protocol](custom-remote-protocol-reference.md)
</dt> <dd>

Contiene interfacce, strutture, unioni e tipi di enumerazione che consentono di creare un Remote Desktop Protocol personalizzato (RDP).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Servizi Desktop remoto](about-terminal-services.md)
</dt> </dl>

 

 




