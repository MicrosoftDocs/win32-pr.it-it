---
description: L'API WiFi nativa contiene un set di funzioni che supportano l'uso di Wi-Fi Direct per le app desktop.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: Informazioni sulla funzionalità Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318266"
---
# <a name="about-the-wi-fi-direct-feature"></a>Informazioni sulla funzionalità Wi-Fi Direct

L'API WiFi nativa contiene un set di funzioni che supportano l'uso di Wi-Fi Direct per le app desktop. A partire da Windows 8 e Windows Server 2012, Wi-Fi funzioni dirette sono state aggiunte all'API WiFi nativa.

La funzionalità Wi-Fi diretta è basata sullo sviluppo della Wi-Fi specifiche tecniche peer-to-Peer v 1.1 da Wi-Fi Alliance (vedere le [specifiche pubblicate in Wi-Fi Alliance](https://www.wi-fi.org/)). L'obiettivo della specifica tecnica peer-to-peer Wi-Fi è fornire una soluzione per Wi-Fi la connettività da dispositivo a dispositivo senza che sia necessario un punto di accesso wireless (AP wireless) per configurare la connessione o l'utilizzo del meccanismo di Wi-Fi ad hoc (IBSS) esistente.

> [!Note]  
> La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows. A partire da Windows 8.1 e Windows Server 2012 R2, usare invece Wi-Fi Direct.

 

Per un'app desktop, la funzionalità Wi-Fi Direct richiede che i dispositivi Wi-FI Direct siano in precedenza abbinati dall'utente con l'interfaccia utente di Windows pairing Experience. Una volta completata questa associazione, viene archiviato un profilo che consente di usare le funzioni dirette di Wi-Fi per avviare una sessione di Wi-Fi Direct per stabilire una connessione tra il Wi-Fi i dispositivi diretti.

Le funzioni seguenti supportano la funzionalità Wi-Fi Direct.

-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indica che l'app vuole annullare una funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) in sospeso che non è stata completata.
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : chiude un handle per il servizio diretto Wi-Fi.
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : chiude una sessione dopo una chiamata precedentemente riuscita alla funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : apre un handle per il servizio Wi-Fi Direct e negozia una versione dell'API Wi-Fi Direct da usare.
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : recupera e applica un profilo archiviato per un dispositivo Wi-Fi Direct legacy.
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : avvia una connessione su richiesta a un dispositivo Wi-Fi diretto specifico, che è stato precedentemente abbinato tramite l'esperienza di abbinamento di Windows.
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : aggiorna la visibilità del dispositivo per l'indirizzo Wi-Fi diretto del dispositivo per un determinato nodo del dispositivo Wi-Fi diretto installato.
-   [**Direttiva \_ di Apri \_ \_ \_ callback completo della sessione**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : definisce la funzione di callback chiamata dalla funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) al completamento dell'operazione **WFDStartOpenSession**

Per ulteriori informazioni sull'utilizzo di Wi-Fi Direct in un'applicazione desktop, vedere [utilizzo delle funzioni Wi-Fi dirette](using-the-wi-fi-direct-api.md).

Per altre informazioni su Wi-Fi Direct per l'uso nelle app di Windows Store, vedere [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) e le classi correlate nello spazio dei nomi [**Windows. Networking. prossimità**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Altre risorse**
</dt> <dt>

[Informazioni sul Wi-Fi nativo](about-native-wifi.md)
</dt> <dt>

[Informazioni sull'API WiFi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Informazioni sull'API ad hoc wireless](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Uso delle funzioni Wi-Fi dirette](using-the-wi-fi-direct-api.md)
</dt> <dt>

**Riferimento**
</dt> <dt>

[**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**\_ \_ callback completo della sessione di apertura della \_ direttiva GMA \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
