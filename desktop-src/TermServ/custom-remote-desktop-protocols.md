---
title: Remote Desktop Protocol Provider API
description: Usare l'API Remote Desktop Protocol provider di servizi per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556d01142c3d46e208b99e1e7e232f11db4cacb600f5bdc0fca37f961cd0f8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001585"
---
# <a name="remote-desktop-protocol-provider-api"></a>Remote Desktop Protocol Provider API

Usare l'API Remote Desktop Protocol provider di servizi per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.

Quando Windows Server viene caricato, viene avviato Servizi Desktop remoto servizio di Gestione connessioni (RCM). Il servizio avvia anche gli oggetti listener per i provider Remote Desktop Protocol che a loro volta sono in ascolto delle connessioni client. Il servizio e i provider di protocollo sono oggetti in modalità utente che comunicano usando le API descritte in questa documentazione. I provider di protocolli possono comunicare con i driver in modalità kernel usando i controlli di input/output (IOCTL). Questo aspetto è illustrato nella figura seguente.

![architettura dell'API del protocollo personalizzato](images/protocol-architecture.png)

Microsoft ha implementato il Remote Desktop Protocol (RDP) per fornire la comunicazione tra il servizio Servizi Desktop remoto e le connessioni client. È possibile creare un protocollo personalizzato usando le interfacce, le strutture, le unioni e i tipi di enumerazione che costituiscono l'API Remote Desktop Protocol Provider. Per ulteriori informazioni, vedere gli argomenti seguenti.

<dl> <dt>

[Creazione di un provider Remote Desktop Protocol](creating-a-custom-remote-protocol.md)
</dt> <dd>

Informazioni sulla creazione di un Remote Desktop Protocol provider. Il gestore di protocollo viene implementato come server COM e registrato in un percorso cercato all'avvio Servizi Desktop remoto servizio.

</dd> <dt>

[Remote Desktop Protocol riferimento al provider](custom-remote-protocol-reference.md)
</dt> <dd>

Contiene interfacce, strutture, unioni e tipi di enumerazione che consentono di creare un Remote Desktop Protocol personalizzato (RDP).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Servizi Desktop remoto](about-terminal-services.md)
</dt> </dl>

 

 




