---
title: Scrittura di uno script per configurare la directory virtuale
description: Scrittura di uno script per configurare la directory virtuale
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae23a33c2c91dc0a141c6f377daf89708499aae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955167"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>Scrittura di uno script per configurare la directory virtuale

Per caricare un file nel server, è possibile utilizzare i valori predefiniti della proprietà IIS BITS. Il file di caricamento viene scritto nell'URL come specificato nel nome file remoto del processo. Per caricare il file in un'applicazione server e ricevere una risposta, modificare la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) per inviare i dati per riferimento (Invia il nome del file che contiene i dati) o per valore (Invia i dati nel corpo della richiesta).

Per un elenco e una descrizione delle proprietà che è possibile modificare, vedere [proprietà dell'estensione IIS BITS](bits-iis-extension-properties.md). Usare i metodi dell'interfaccia [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) per abilitare e disabilitare la directory virtuale per i caricamenti.

Nell'esempio seguente viene illustrato come utilizzare Windows script host per creare, configurare e abilitare una directory virtuale IIS per i caricamenti BITS.


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

//Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



Per modificare l'esempio precedente in modo da caricare i dati in un'applicazione server, aggiungere il codice seguente prima di **SetInfo**.


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



Il percorso del file di caricamento viene passato all'applicazione server myasp. asp nell'intestazione BITS-request-DataFile-Name. Per ricevere il file di caricamento nel corpo della richiesta, impostare la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) su 2.

Per informazioni sulla ricezione dei dati di caricamento nell'applicazione server, vedere [uso delle intestazioni di richiesta/risposta per le notifiche BITS](using-bits-notification-request-response-headers.md).

 

 




