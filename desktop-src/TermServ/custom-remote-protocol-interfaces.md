---
title: Interfacce del provider Remote Desktop Protocol
description: Interfacce supportate dall'API del provider Remote Desktop Protocol.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955058"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Interfacce del provider Remote Desktop Protocol

Le interfacce seguenti sono supportate dall'API del provider Remote Desktop Protocol.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Espone i metodi chiamati dal servizio Servizi Desktop remoto per configurare una connessione client.

</dd> <dt>

[**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Espone metodi che forniscono informazioni sullo stato di una connessione client e che eseguono azioni per il client. Questa interfaccia viene implementata dal servizio Servizi Desktop remoto e chiamata dal protocollo.

</dd> <dt>

[**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Espone i metodi utilizzati dal servizio Servizi Desktop remoto per eseguire l'handshake delle licenze durante una sequenza di connessione.

</dd> <dt>

[**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Espone i metodi che richiedono che il protocollo avvii e arresti l'ascolto delle richieste di connessione client.

</dd> <dt>

[**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Espone metodi che notificano al servizio Servizi Desktop remoto che un client è connesso.

</dd> <dt>

[**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Espone i metodi chiamati dal servizio Servizi Desktop remoto per aggiornare lo stato di accesso e determinare come indirizzare i messaggi di errore di accesso.

</dd> <dt>

[**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Espone metodi che il servizio Servizi Desktop remoto utilizza per comunicare con il provider del protocollo.

</dd> <dt>

[**IWRdsProtocolSettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Espone metodi per il recupero e l'aggiunta di impostazioni relative ai criteri.

</dd> <dt>

[**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Espone i metodi chiamati dal protocollo per notificare al servizio Servizi Desktop remoto di avviare o arrestare il lato di destinazione di un'ombreggiatura.

</dd> <dt>

[**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Espone metodi che notificano al provider del protocollo lo stato di shadowing della sessione.

</dd> <dt>

[**IWRdsRemoteFXGraphicsConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Espone metodi relativi alla manipolazione e alla comprensione della grafica nella connessione client.

</dd> <dt>

[Interfacce del provider di protocollo desktop deprecate](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

Le interfacce seguenti sono state deprecate e non devono più essere utilizzate. Per i nuovi progetti, usare invece le interfacce del provider di Remote Desktop Protocol.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al provider Remote Desktop Protocol](custom-remote-protocol-reference.md)
</dt> <dt>

[Enumerazioni del provider Remote Desktop Protocol](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Strutture del provider Remote Desktop Protocol](custom-remote-protocol-structures.md)
</dt> <dt>

[Unioni provider Remote Desktop Protocol](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




