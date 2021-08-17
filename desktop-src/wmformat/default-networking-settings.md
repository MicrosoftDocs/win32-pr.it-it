---
title: Impostazioni di rete Impostazioni
description: Impostazioni di rete Impostazioni
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media Format SDK, impostazioni di rete predefinite
- Advanced Systems Format (ASF), impostazioni di rete predefinite
- ASF (Advanced Systems Format), impostazioni di rete predefinite
- Windows MEDIA Format SDK, impostazioni di rete
- Advanced Systems Format (ASF), impostazioni di rete
- ASF (Advanced Systems Format), impostazioni di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591bf4aa2154d5cc04a8a17b5fc75f290a8493a39d530d4246bc0338c2424e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931421"
---
# <a name="default-networking-settings"></a>Impostazioni di rete Impostazioni

Le tabelle seguenti descrivono le impostazioni predefinite dei parametri di rete in Windows Media Format SDK, raggruppate per interfaccia.



| IWMReaderNetworkConfig                | Impostazione predefinita              |
|---------------------------------------|------------------------------|
| Tempo di memorizzazione nel buffer                        | 5 secondi                    |
| UseFixedUDPPort                       | FALSE                        |
| FixedUDPPort                          | 0 (non valido)                |
| ProxySetting: HTTP                    | BROWSER DELLE IMPOSTAZIONI PROXY WMT \_ \_ \_ |
| ProxySetting: MMS                     | IMPOSTAZIONE PROXY WMT \_ \_ \_ NONE    |
| ProxySetting: RTSP                    | IMPOSTAZIONE PROXY WMT \_ \_ \_ NONE    |
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
| Larghezza di banda della connessione                  | 0 (rilevamento automatico)              |



 



| IWMReaderNetworkConfig2        | Impostazione predefinita        |
|--------------------------------|------------------------|
| Durata dello streaming accelerato | 100000000 (10 secondi) |
| Abilitare la memorizzazione nella cache del contenuto         | true                   |
| Abilitare la cache veloce              | true                   |
| Abilitare i reinvii                 | true                   |
| Abilitare il thinning del contenuto        | true                   |
| Limite di riconnessione                | 25                     |



 



| IWMWriterNetworkSink | Impostazione predefinita         |
|----------------------|-------------------------|
| Numero massimo di client      | 5                       |
| Protocollo di rete     | 0 (PROTOCOLLO WMT \_ \_ HTTP) |
| Host URL             | 0 (non valido)           |



 



| IWMWriterAdvanced2  | Impostazione predefinita             |
|---------------------|-----------------------------|
| Dimensioni massime del pacchetto | 1400                        |
| Log client ID       | FALSE                       |
| Modalità di riproduzione           | SELEZIONE AUTOMATICA \_ DELLA \_ MODALITÀ DI RIPRODUZIONE WMT \_ |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione della funzionalità di rete**](implementing-network-functionality.md)
</dt> </dl>

 

 




