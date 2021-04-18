---
description: Viene illustrato l'utilizzo di funzioni di rete ospitate senza fili.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Esempio di rete wireless ospitata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307724"
---
# <a name="wireless-hosted-network-sample"></a>Esempio di rete wireless ospitata

Un esempio di rete wireless ospitata che illustra l'utilizzo delle funzioni di rete ospitata senza fili è incluso in Microsoft Windows Software Development Kit (SDK). La versione più recente del Windows SDK è disponibile nell' [area download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

Per impostazione predefinita, il codice sorgente di esempio di rete wireless ospitata è installato nella directory seguente:

**C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ NetDs \\ WLAN**

L'esempio wireless Hosted Network si trova nella cartella seguente:

**WirelessHostedNetwork**

È possibile compilare l'esempio wireless Hosted Network nell'Windows SDK per Windows 7. L'esempio wireless Hosted Network può essere eseguito in Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato.

In Windows 7 e in Windows Server 2008 R2 con il servizio LAN wireless installato, il sistema operativo installa un dispositivo virtuale se nel computer è presente una scheda di rete ospitata che supporta la connessione wireless. Questo dispositivo virtuale viene normalmente visualizzato nella "cartella connessioni di rete" come "connessione di rete wireless 2" con il nome del dispositivo "Microsoft Virtual WiFi Miniport Adapter" Se il computer dispone di una singola scheda di rete wireless. Questo dispositivo virtuale viene usato esclusivamente per eseguire le connessioni del punto di accesso software (SoftAP). La durata del dispositivo virtuale è legata alla scheda wireless fisica. Se la scheda fisica wireless è disabilitata, verrà rimosso anche questo dispositivo virtuale.

Le funzioni di rete ospitata senza fili vengono utilizzate per avviare e arrestare la rete ospitata senza fili, configurare o modificare le impostazioni oppure eseguire una query per ottenere informazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla rete wireless ospitata](about-the-wireless-hosted-network.md)
</dt> <dt>

[Uso della condivisione connessione Internet e della rete ospitata](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



