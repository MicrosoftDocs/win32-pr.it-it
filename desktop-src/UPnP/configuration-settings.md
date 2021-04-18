---
title: Impostazioni di configurazione
description: Il comportamento dell'API del punto di controllo e dell'API host del dispositivo può essere modificato modificando le impostazioni nel registro di sistema.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297941"
---
# <a name="configuration-settings"></a>Impostazioni di configurazione

Il comportamento dell'API del [punto di controllo](control-point-api.md) e dell' [API host del dispositivo](device-host-api.md) può essere modificato modificando le impostazioni nel registro di sistema.

Sono presenti sette valori del registro di sistema che influiscono sul comportamento:

-   **DownloadScope**
-   **DeviceLifeTime**
-   \\**Host** \\ dispositivo UPnP **Limite dimensioni file**
-   \\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite dimensioni file**
-   **MaxCache**
-   **TTL**
-   **ReceiveScope**

Sono presenti due valori del registro di sistema denominati **limite dimensioni file**, uno per i documenti di descrizione e l'altro per le risposte che usano Simple Object Access Protocol (SOAP).

Il percorso di ognuno dei sette valori nel registro di sistema è il seguente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a>Descrizioni del valore del registro di sistema

I valori del registro di sistema sono illustrati nell'elenco seguente. Ogni valore del registro di sistema è **reg \_ DWORD** (un numero intero a 32 bit). L'effetto di ogni valore è globale.

<dl> <dt>

<span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**
</dt> <dd>

Specifica gli indirizzi IP validi per l'URL del documento di descrizione del dispositivo. Se l'indirizzo IP dell'host specificato nell'URL del documento di descrizione non è compreso nell'ambito specificato da **DownloadScope**, l'indirizzo IP non è valido e l'oggetto dispositivo non verrà creato.

I valori validi sono riportati nella tabella seguente. Il valore predefinito è 1.



| Valore di **DownloadScope** | Significato                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                          | L'indirizzo IP dell'host deve essere un indirizzo subnet.                                                                                                                                                                |
| 1                          | L'indirizzo IP dell'host deve essere un indirizzo di subnet o un indirizzo privato, ovvero uno dei 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (come specificato da RFC 1918) o 169,254. *x*. *x* (come specificato da RFC 3330). |
| 2                          | L'indirizzo IP dell'host deve essere un indirizzo di subnet, un indirizzo privato o un indirizzo che rientra negli hop TTL (time-to-Live) dal punto di controllo.                                                              |
| 3                          | L'indirizzo IP dell'host può essere qualsiasi indirizzo.                                                                                                                                                                      |
| >3                      | Uguale a quello per il valore 0.                                                                                                                                                                              |



 

</dd> <dt>

<span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**
</dt> <dd>

facoltativo. Specifica la durata, in secondi, del dispositivo che sostituisce il valore specificato nel messaggio di annuncio del dispositivo. Se **DeviceLifeTime** è presente, il valore specificato nell'annuncio del dispositivo viene ignorato e viene invece usato il valore del registro di sistema. Questo vale per tutti i dispositivi.

I valori validi sono compresi tra 900 e **Max \_ DWORD**. Il valore predefinito è 1800. Se **DeviceLifeTime** è impostato su 0, viene usato il valore predefinito.

</dd> <dt>

<span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**Host** \\ dispositivo UPnP **Limite dimensioni file**
</dt> <dd>

Specifica la dimensione massima, in byte, di ogni documento di descrizione. Questa impostazione non è configurabile nelle versioni di Windows precedenti a Windows XP Service Pack 2. Nelle versioni precedenti questa impostazione è hardcoded come 102400.

I valori validi sono compresi tra 10240 e **Max \_ DWORD**. Il valore predefinito è 102400.

</dd> <dt>

<span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite dimensioni file**
</dt> <dd>

Specifica la dimensione massima, in byte, della risposta SOAP accettabile. Questa impostazione non è configurabile nelle versioni di Windows precedenti a Windows XP Service Pack 2. Nelle versioni precedenti questa impostazione è hardcoded come 102400.

I valori validi sono compresi tra 10240 e **Max \_ DWORD**. Il valore predefinito è 102400.

</dd> <dt>

<span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**
</dt> <dd>

Specifica il numero massimo di voci consentite nella cache Simple Service Discovery Protocol (SSDP).

I valori validi sono compresi tra 10 e 30000. Il valore predefinito è 1000.

</dd> <dt>

<span id="TTL"></span><span id="ttl"></span>**TTL**
</dt> <dd>

Specifica la durata (TTL) per un pacchetto SSDP. Ovvero **TTL** specifica il numero di hop consentiti per un pacchetto.

I valori validi sono compresi tra 1 e 255. Il valore predefinito è 1.

</dd> <dt>

<span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**
</dt> <dd>

Specifica quali indirizzi IP sono origini valide di un messaggio. Se un messaggio in ingresso proviene da un indirizzo non compreso nell'ambito specificato da **ReceiveScope**, il messaggio viene ignorato. Questa impostazione non è configurabile nelle versioni di Windows precedenti a Windows XP Service Pack 2. Nelle versioni precedenti un messaggio viene accettato indipendentemente dalla relativa origine.

I valori validi sono riportati nella tabella seguente. Il valore predefinito è 1.



| Valore di **ReceiveScope** | Significato                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                         | L'indirizzo IP del mittente deve essere un indirizzo subnet.                                                                                                                                                                |
| 1                         | L'indirizzo IP del mittente deve essere un indirizzo di subnet o un indirizzo privato, ovvero uno dei 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (come specificato da RFC 1918) o 169,254. *x*. *x* (come specificato da RFC 3330). |
| 2                         | Non usato. Se **ReceiveScope** è impostato su 2, viene usato il valore predefinito.                                                                                                                                        |
| 3                         | L'indirizzo IP del mittente può essere qualsiasi indirizzo.                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'architettura UPnP](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




