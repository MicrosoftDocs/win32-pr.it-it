---
title: Registrazione di Protocol Manager
description: È necessario creare almeno una voce del valore del Registro di sistema per il gestore di protocollo in modo che il Servizi Desktop remoto possa crearne un'istanza.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851fe74d7e22a068eccd0d901cab14d754b6b2364611bfdda2aecd68dcf224d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988791"
---
# <a name="registering-the-protocol-manager"></a>Registrazione di Protocol Manager

È necessario creare almeno una voce del valore del Registro di sistema per il gestore di protocollo in modo che il Servizi Desktop remoto possa crearne un'istanza.

## <a name="registry-location"></a>Percorso del registro

Creare una chiave del Registro di sistema nel percorso seguente per ogni listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) che viene utilizzato dal protocollo. In questo esempio le nuove chiavi del listener sono denominate *MyListener1* e *MyListener2.*

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

Per riferimento, è possibile visualizzare le voci di valore nella chiave del listener **RDP-Tcp** predefinita in questo percorso.

## <a name="registry-value-entries"></a>Voci dei valori del Registro di sistema

La chiave del listener per il protocollo deve avere una voce di valore denominata **LoadableProtocol \_ Object**<dl> <dt>

Tipo di dati
</dt> <dd>REG_SZ</dd> </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**Interfaccia IWRdsProtocolManager.**</a> Il Servizi Desktop remoto utilizza questo CLSID per creare un'istanza del gestore di protocollo per questo listener dopo aver trovato il listener nel Registro di sistema.

Se il provider di protocolli usa più di un listener, il servizio Servizi Desktop remoto crea una sola istanza del gestore di protocolli e la usa per chiamare [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) una volta per ogni listener.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider Remote Desktop Protocol](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Sequenza di chiamata al metodo](method-call-sequence.md)
</dt> </dl>

 

 




