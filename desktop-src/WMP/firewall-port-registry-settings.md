---
title: Impostazioni del registro di sistema della porta del firewall
description: Impostazioni del registro di sistema della porta del firewall
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, impostazioni del registro di sistema della porta firewall
- Windows Media Player, impostazioni del registro di sistema della porta
- Windows Media Player, registro di sistema
- Registro di sistema, impostazioni della porta del firewall
- Registro di sistema, impostazioni porta
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema della porta del firewall
- impostazioni del registro di sistema della porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855565"
---
# <a name="firewall-port-registry-settings"></a>Impostazioni del registro di sistema della porta del firewall

Windows Media Player inserisce le voci nel registro di sistema in modo che i firewall possano determinare se aprire o chiudere le porte utilizzate dalla condivisione del catalogo multimediale.

**Voce del registro di sistema AcceptedEULA**

Windows Media Player utilizza la seguente voce del registro di sistema per indicare se l'utente ha accettato il contratto di licenza con l'utente finale (EULA).


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



Il valore 1 indica che l'utente ha accettato il contratto di licenza. Il valore 0 indica che l'utente non ha accettato il contratto di licenza.

**Voce del registro di sistema WMPNSSFirewallPortsOpen**

Windows Media Player utilizza la seguente voce del registro di sistema per indicare se l'utente ha scelto di condividere la propria libreria multimediale con altri computer in una rete domestica.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



Il valore 1 indica che l'utente ha scelto di condividere la libreria. Il valore 0 indica che l'utente ha scelto di non condividere la libreria.

**Porte correlate alla condivisione del catalogo multimediale**

In Windows Vista, se la voce del registro di sistema **WMPNSSFirewallPortsOpen** ha un valore pari a 1, è necessario aprire le porte seguenti.



| Porta          | Protocollo                  | Processo                         | Direzione            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | RTSP TCP                  | wmpnetwk.exe                    | in ingresso e in uscita |
| 8554-8558   | RTSP TCP                  | wmpnetwk.exe                    | in ingresso e in uscita |
| 5004, 5005    | RTCP/RTP UDP              | wmpnetwk.exe                    | in ingresso e in uscita |
| 50004-50013 | RTCP/RTP UDP              | wmpnetwk.exe                    | in ingresso e in uscita |
| 1900          | SSDP UDP                  | SSDPsrv in svchost.exe          | in ingresso e in uscita |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost in svchost.exe | in entrata              |
| 10280-10284 | Registrazione UDP WMDRM-ND | wmpnetwk.exe                    | in ingresso e in uscita |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | in entrata              |
| 2177          | QWAVE UDP TCP             | svchost.exe                     | in ingresso e in uscita |



 

In Windows Vista, se la voce del registro di sistema **AcceptedEULA** ha un valore pari a 1, è necessario aprire le porte seguenti.



| Porta          | Protocollo       | Processo                         | Direzione            |
|---------------|----------------|---------------------------------|----------------------|
| Tutte le porte UDP | RTP UDP, MSB   | wmplayer.exe, qualsiasi subnet        | in entrata              |
| 1900          | SSDP UDP       | SSDPsrv/UPnPHost in svchost.exe | in ingresso e in uscita |
| 2869          | TCP SSDP, UPnP | SSDPsrv, UPnPHost               | in entrata              |



 

In Microsoft Windows XP, se la voce del registro di sistema **WMPNSSFirewallPortsOpen** ha un valore pari a 1, è necessario aprire le porte seguenti.



| Porta          | Protocollo                  | Processo                         | Direzione            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1900          | SSDP UDP                  | SSDPsrv in svchost.exe          | in ingresso e in uscita |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost in svchost.exe | in entrata              |
| 10280-10284 | Registrazione UDP WMDRM-ND | wmpnetwk.exe                    | in ingresso e in uscita |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | in entrata              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema**](registry-settings.md)
</dt> </dl>

 

 




