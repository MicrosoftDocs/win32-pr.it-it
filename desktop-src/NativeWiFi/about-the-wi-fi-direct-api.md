---
description: L'API Wi-Fi nativa contiene un set di funzioni che supportano l'uso di Wi-Fi Direct per le app desktop.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: Informazioni sulla Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2816938b3e2d9156f2a97b67990386af2d5d780aa0226316cccc5edd0f2a4b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620209"
---
# <a name="about-the-wi-fi-direct-feature"></a>Informazioni sulla Wi-Fi Direct

L'API Wi-Fi nativa contiene un set di funzioni che supportano l'uso di Wi-Fi Direct per le app desktop. A partire Windows 8 e Windows Server 2012, Wi-Fi funzioni Direct sono state aggiunte all'API Wi-Fi nativa.

La funzionalità Wi-Fi Direct si basa sullo sviluppo della specifica tecnica peer-to-peer v1.1 di Wi-Fi di Wi-Fi Alliance (vedere Le specifiche pubblicate di [Wi-Fi Alliance).](https://www.wi-fi.org/) L'obiettivo della specifica tecnica peer-to-peer di Wi-Fi è quello di fornire una soluzione per la connettività da dispositivo a dispositivo di Wi-Fi senza la necessità di un punto di accesso wireless per configurare la connessione o l'uso del meccanismo ad hoc Wi-Fi (IBSS) esistente.

> [!Note]  
> La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows. A partire Windows 8.1 e Windows Server 2012 R2, usare Wi-Fi Direct.

 

Per un'app desktop, la funzionalità Wi-Fi Direct richiede che i dispositivi Wi-FI Direct siano precedentemente associati dall'utente all'interfaccia utente dell'esperienza di Windows pairing. Al termine dell'associazione, viene archiviato un profilo che consente di usare le funzioni di Wi-Fi Direct per avviare una sessione di Wi-Fi Direct per stabilire una connessione tra i dispositivi Wi-Fi Direct.

Le funzioni seguenti supportano la Wi-Fi Direct.

-   [**WFDCancelOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) indica che l'app vuole annullare una funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) in sospeso che non è stata completata.
-   [**WFDCloseHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) chiude un handle al Wi-Fi Direct.
-   [**WFDCloseSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) chiude una sessione dopo una chiamata riuscita in precedenza alla [**funzione WFDStartOpenSession.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDOpenHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) apre un handle per il servizio Wi-Fi Direct e negozia una versione dell'API Wi-FI Direct da usare.
-   [**WFDOpenLegacySession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) recupera e applica un profilo archiviato per un dispositivo legacy Wi-Fi Direct.
-   [**WFDStartOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) avvia una connessione su richiesta a un dispositivo Wi-Fi Direct specifico, precedentemente associato tramite l'esperienza di associazione Windows dispositivi.
-   [**WFDUpdateDeviceVisibility:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) aggiorna la visibilità del dispositivo Wi-Fi'indirizzo del dispositivo diretto per un determinato nodo Wi-Fi dispositivo direct.
-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : definisce la funzione di callback chiamata dalla funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) al completamento dell'operazione **WFDStartOpenSession**

Per altre informazioni sull'uso Wi-Fi Direct in un'app desktop, vedere [Uso delle Wi-Fi Direct.](using-the-wi-fi-direct-api.md)

Per altre informazioni su Wi-Fi Direct per l'uso nelle app di Windows Store, vedere [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) e le classi correlate [**nel Windows. Spazio dei nomi Networking.Proximity.**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Altre risorse**
</dt> <dt>

[Informazioni sul Wi-Fi nativo](about-native-wifi.md)
</dt> <dt>

[Informazioni sull'API Wi-Fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Informazioni sull'API ad hoc wireless](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Uso delle Wi-Fi Direct](using-the-wi-fi-direct-api.md)
</dt> <dt>

**Riferimento**
</dt> <dt>

[**Peerfinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**CALLBACK DI APERTURA \_ \_ SESSIONE WFD \_ \_ COMPLETATO**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
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

 

 
