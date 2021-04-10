---
title: Impostazioni di rete predefinite
description: Impostazioni di rete predefinite
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media Format SDK, impostazioni di rete predefinite
- ASF (Advanced Systems Format), impostazioni di rete predefinite
- ASF (formato avanzato dei sistemi), impostazioni di rete predefinite
- Windows Media Format SDK, impostazioni di rete
- ASF (Advanced Systems Format), impostazioni di rete
- ASF (formato avanzato dei sistemi), impostazioni di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856925"
---
# <a name="default-networking-settings"></a>Impostazioni di rete predefinite

Le tabelle seguenti descrivono le impostazioni predefinite dei parametri di rete in Windows Media Format SDK, raggruppate per interfaccia.



| IWMReaderNetworkConfig                | Impostazione predefinita              |
|---------------------------------------|------------------------------|
| Tempo di memorizzazione nel buffer                        | 5 secondi                    |
| UseFixedUDPPort                       | FALSE                        |
| FixedUDPPort                          | 0 (non valido)                |
| ProxySetting: HTTP                    | \_ \_ browser impostazioni proxy \_ WMT |
| ProxySetting: MMS                     | \_impostazione del proxy WMT \_ \_ None    |
| ProxySetting: RTSP                    | \_impostazione del proxy WMT \_ \_ None    |
| ProxyHostName (HTTP, MMS, RTSP)       | ""                           |
| ProxyPort: HTTP                       | 80                           |
| ProxyPort: MMS                        | 1755                         |
| ProxtPort: RTSP                       | 554                          |
| ProxyExceptionList (HTTP, MMS, RTSP)  | ""                           |
| ProxyBypassForLocal (HTTP, MMS, RTSP) | FALSE                        |
| ForceRerunAutoDetection               | FALSE                        |
| EnableMulticast                       | true                         |
| EnableHTTP                            | true                         |
| EnableTCP                             | true                         |
| EnableUDP                             | true                         |
| Larghezza di banda di connessione                  | 0 (rilevamento automatico)              |



 



| IWMReaderNetworkConfig2        | Impostazione predefinita        |
|--------------------------------|------------------------|
| Durata flusso accelerato | 100 milioni (10 secondi) |
| Abilita Caching contenuto         | true                   |
| Abilita cache veloce              | true                   |
| Abilita reinvii                 | true                   |
| Abilita l'assottigliamento del contenuto        | true                   |
| Limite riconnessione                | 25                     |



 



| IWMWriterNetworkSink | Impostazione predefinita         |
|----------------------|-------------------------|
| Numero massimo di client      | 5                       |
| Protocollo di rete     | 0 ( \_ protocollo \_ http WMT) |
| URL host             | 0 (non valido)           |



 



| IWMWriterAdvanced2  | Impostazione predefinita             |
|---------------------|-----------------------------|
| Dimensioni massime pacchetto | 1400                        |
| ID client di log       | FALSE                       |
| Modalità di riproduzione           | \_ \_ \_ selezione autoselezione modalità di riproduzione WMT |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione della funzionalità di rete**](implementing-network-functionality.md)
</dt> </dl>

 

 




