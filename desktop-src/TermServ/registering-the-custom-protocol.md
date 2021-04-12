---
title: Registrazione di gestione protocolli
description: È necessario creare almeno una voce del valore del registro di sistema per gestione protocolli, in modo che il servizio Servizi Desktop remoto possa crearne un'istanza.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395623"
---
# <a name="registering-the-protocol-manager"></a>Registrazione di gestione protocolli

È necessario creare almeno una voce del valore del registro di sistema per gestione protocolli, in modo che il servizio Servizi Desktop remoto possa crearne un'istanza.

## <a name="registry-location"></a>Percorso del registro

Creare una chiave del registro di sistema nel percorso seguente per ogni listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) usato dal protocollo. In questo esempio le nuove chiavi del listener sono denominate *MyListener1* e *MyListener2*.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

Come riferimento, è possibile visualizzare le voci di valore sotto la chiave del listener **RDP-TCP** predefinito in questo percorso.

## <a name="registry-value-entries"></a>Voci del valore del registro di sistema

La chiave del listener per il protocollo deve avere una voce di valore denominata **\_ oggetto LoadableProtocol**<dl> <dt>

Tipo di dati
</dt> <dd>REG_SZ</dd> Interfaccia </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> .) Il servizio Servizi Desktop remoto utilizza questo CLSID per creare un'istanza del gestore di protocollo per questo listener dopo aver trovato il listener nel registro di sistema.

Se il provider del protocollo usa più di un listener, il servizio Servizi Desktop remoto crea solo un'istanza di gestione protocolli e la usa per chiamare [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) una volta per ogni listener.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di Remote Desktop Protocol](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Sequenza di chiamate al metodo](method-call-sequence.md)
</dt> </dl>

 

 




