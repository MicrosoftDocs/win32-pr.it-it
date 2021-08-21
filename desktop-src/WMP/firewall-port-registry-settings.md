---
title: Registro delle porte del firewall Impostazioni
description: Registro delle porte del firewall Impostazioni
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player,impostazioni del Registro di sistema delle porte del firewall
- Windows Media Player,impostazioni del Registro di sistema delle porte
- Windows Media Player,registro
- Registro di sistema, impostazioni delle porte del firewall
- Registro di sistema, impostazioni delle porte
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del Registro di sistema per le porte del firewall
- impostazioni del Registro di sistema delle porte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140f55a4008a03c2b3bc4184e2eca92129a5e30dc69f0871da856b4555daec73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576768"
---
# <a name="firewall-port-registry-settings"></a>Registro delle porte del firewall Impostazioni

Windows Media Player inserisce le voci nel Registro di sistema in modo che i firewall possano determinare se aprire o chiudere le porte usate dalla condivisione del catalogo multimediale.

**Voce del Registro di sistema AcceptedEULA**

Windows Media Player usa la voce del Registro di sistema seguente per indicare se l'utente ha accettato il contratto di licenza con l'utente finale.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



Il valore 1 indica che l'utente ha accettato il contratto di licenza. Il valore 0 indica che l'utente non ha accettato il contratto di licenza.

**Voce del Registro di sistema WMPNSSFirewallPortsOpen**

Windows Media Player usa la voce del Registro di sistema seguente per indicare se l'utente ha scelto di condividere il proprio catalogo multimediale con altri computer in una rete domestica.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



Il valore 1 indica che l'utente ha scelto di condividere la libreria. Il valore 0 indica che l'utente ha scelto di non condividere la libreria.

**Porte correlate alla condivisione del catalogo multimediale**

In Windows Vista, se la voce del Registro di sistema **WMPNSSFirewallPortsOpen** ha un valore pari a 1, devono essere aperte le porte seguenti.



| Porta          | Protocollo                  | Processo                         | Direzione            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | TCP RTSP                  | wmpnetwk.exe                    | in ingresso e in uscita |
| 8554 - 8558   | TCP RTSP                  | wmpnetwk.exe                    | in ingresso e in uscita |
| 5004, 5005    | UDP RTCP/RTP              | wmpnetwk.exe                    | in ingresso e in uscita |
| 50004 - 50013 | UDP RTCP/RTP              | wmpnetwk.exe                    | in ingresso e in uscita |
| 1900          | UDP SSDP                  | SSDPsrv in svchost.exe          | in ingresso e in uscita |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost in svchost.exe | in entrata              |
| 10280 - 10284 | Registrazione WMDRM-ND UDP | wmpnetwk.exe                    | in ingresso e in uscita |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | in entrata              |
| 2177          | TCP UDP qWAVE             | svchost.exe                     | in ingresso e in uscita |



 

In Windows Vista, se il valore della voce del Registro di sistema **AcceptedEULA** è 1, devono essere aperte le porte seguenti.



| Porta          | Protocollo       | Processo                         | Direzione            |
|---------------|----------------|---------------------------------|----------------------|
| Tutte le porte UDP | UDP RTP, MSB   | wmplayer.exe, qualsiasi subnet        | in entrata              |
| 1900          | UDP SSDP       | SSDPsrv/UPnPHost in svchost.exe | in ingresso e in uscita |
| 2869          | TCP SSDP, UPnP | SSDPsrv, UPnPHost               | in entrata              |



 

In Microsoft Windows XP, se il valore della voce del Registro di sistema **WMPNSSFirewallPortsOpen** è 1, devono essere aperte le porte seguenti.



| Porta          | Protocollo                  | Processo                         | Direzione            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1900          | UDP SSDP                  | SSDPsrv in svchost.exe          | in ingresso e in uscita |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost in svchost.exe | in entrata              |
| 10280 - 10284 | Registrazione WMDRM-ND UDP | wmpnetwk.exe                    | in ingresso e in uscita |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | in entrata              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Registro di sistema Impostazioni**](registry-settings.md)
</dt> </dl>

 

 




