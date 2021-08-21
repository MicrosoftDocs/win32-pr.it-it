---
title: Remote Desktop Protocol provider di servizi
description: Interfacce supportate dall'API Remote Desktop Protocol provider.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bde36cb70f937559dce20a73a485ec109a2cf6c6ae6c687655963c70e6ce22b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681231"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Remote Desktop Protocol provider di servizi

Le interfacce seguenti sono supportate dall'API Remote Desktop Protocol provider.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Espone i metodi chiamati dal Servizi Desktop remoto per configurare una connessione client.

</dd> <dt>

[**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Espone metodi che forniscono informazioni sullo stato di una connessione client e che eseguono azioni per il client. Questa interfaccia viene implementata dal Servizi Desktop remoto e chiamata dal protocollo .

</dd> <dt>

[**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Espone i metodi usati dal servizio Servizi Desktop remoto per eseguire l'handshake di licenza durante una sequenza di connessione.

</dd> <dt>

[**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Espone metodi che richiedono l'avvio e l'arresto dell'ascolto delle richieste di connessione client da parte del protocollo.

</dd> <dt>

[**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Espone metodi che notificano al Servizi Desktop remoto che un client è connesso.

</dd> <dt>

[**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Espone i metodi chiamati dal servizio di Servizi Desktop remoto per aggiornare lo stato di accesso e determinare come indirizzare i messaggi di errore di accesso.

</dd> <dt>

[**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Espone i metodi utilizzati dal Servizi Desktop remoto per comunicare con il provider di protocollo.

</dd> <dt>

[**IWRdsProtocolSettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Espone metodi per il recupero e l'aggiunta di impostazioni correlate ai criteri.

</dd> <dt>

[**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Espone i metodi chiamati dal protocollo per notificare al Servizi Desktop remoto di avviare o arrestare il lato di destinazione di un'ombreggiatura.

</dd> <dt>

[**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Espone metodi che notificano al provider di protocollo lo stato dello shadowing della sessione.

</dd> <dt>

[**IWRdsRemoteFXGraphicsConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Espone i metodi relativi alla manipolazione e alla comprensione della grafica nella connessione client.

</dd> <dt>

[Interfacce del provider desktop protocol deprecate](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

Le interfacce seguenti sono deprecate e non devono più essere usate. Per i nuovi progetti, usare Remote Desktop Protocol interfacce provider.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Remote Desktop Protocol riferimento al provider](custom-remote-protocol-reference.md)
</dt> <dt>

[enumerazioni Remote Desktop Protocol provider di dati](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Remote Desktop Protocol provider di servizi](custom-remote-protocol-structures.md)
</dt> <dt>

[Remote Desktop Protocol unioni di provider di servizi](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




