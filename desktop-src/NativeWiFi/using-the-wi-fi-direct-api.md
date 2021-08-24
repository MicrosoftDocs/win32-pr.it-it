---
description: Illustra come usare le Wi-Fi Direct nelle app desktop.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Uso delle Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9a00a5474632ed54a84a7dc8cc5c64774e7cfe7547e6994acee599df2461ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684731"
---
# <a name="using-the-wi-fi-direct-functions"></a>Uso delle Wi-Fi Direct

Questo argomento illustra come usare le Wi-Fi Direct nelle app desktop. A partire Windows 8 e Windows Server 2012, Wi-Fi funzioni Direct sono state aggiunte all'API Wi-Fi nativa.

La funzionalità Wi-Fi Direct si basa sullo sviluppo della specifica tecnica peer-to-peer di Wi-Fi v1.1 di Wi-Fi Alliance (vedere Le specifiche pubblicate di [Wi-Fi Alliance).](https://www.wi-fi.org/) L'obiettivo della specifica tecnica peer-to-peer di Wi-Fi è fornire una soluzione per la connettività da dispositivo a dispositivo di Wi-Fi senza la necessità di un punto di accesso wireless (AP wireless) per configurare la connessione o l'uso del meccanismo ad hoc Wi-Fi (IBSS) esistente.

> [!Note]  
> La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows. A partire Windows 8.1 e Windows Server 2012 R2, usare Wi-Fi Direct.

 

Le funzioni seguenti supportano la Wi-Fi Direct.

-   [**WFDCancelOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) indica che l'app vuole annullare una funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) in sospeso che non è stata completata.
-   [**WFDCloseHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) chiude un handle per il Wi-Fi Direct.
-   [**WFDCloseSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) chiude una sessione dopo una chiamata riuscita in precedenza alla [**funzione WFDStartOpenSession.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDOpenHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) apre un handle per il servizio Wi-Fi Direct e negozia una versione dell'API Wi-FI Direct da usare.
-   [**WFDOpenLegacySession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) recupera e applica un profilo archiviato per Wi-Fi dispositivo legacy direct.
-   [**WFDStartOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) avvia una connessione su richiesta a un dispositivo Wi-Fi Direct specifico, precedentemente associato tramite l'esperienza di Windows dispositivi.
-   [**WFDUpdateDeviceVisibility:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) aggiorna la visibilità del dispositivo per Wi-Fi indirizzo del dispositivo diretto per un determinato nodo Wi-Fi dispositivo Direct.
-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : definisce la funzione di callback chiamata dalla funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) al completamento dell'operazione **WFDStartOpenSession**

Per un'app desktop, la funzionalità Wi-Fi Direct richiede che i dispositivi Wi-FI Direct siano precedentemente associati dall'utente all'interfaccia utente dell'esperienza di Windows pairing. Al termine dell'associazione, viene archiviato un profilo che consente di usare le funzioni di Wi-Fi Direct per avviare una sessione di Wi-Fi Direct per stabilire una connessione tra i dispositivi Wi-Fi Direct.

Per usare Wi-Fi Direct, un'app deve prima ottenere un handle per il servizio Wi-Fi Direct chiamando la [**funzione WFDOpenHandle.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) L'handle Wi-Fi Direct (WFD) restituito dalla funzione **WFDOpenHandle** viene usato per le chiamate di funzione Wi-Fi Direct successive effettuate al servizio Wi-Fi Direct.

La [**funzione WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) avvia un'operazione asincrona per avviare una connessione su richiesta a un dispositivo Wi-Fi Direct. Il dispositivo Wi-Fi di destinazione deve essere stato associato in precedenza tramite l'esperienza di Windows di associazione. Al termine dell'operazione asincrona, viene chiamata la funzione di callback specificata nel parametro *pfnCallback.*

Dopo aver eseguito un'applicazione usando il servizio Wi-Fi Direct, l'applicazione deve chiamare la funzione [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) per segnalare al servizio Wi-Fi Direct che l'applicazione viene eseguita usando il servizio. Ciò consente al Wi-Fi Direct di rilasciare le risorse usate dall'applicazione.

Per altre informazioni su Wi-Fi Direct per l'uso nelle app di Windows Store, vedere [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) e le classi correlate [**nel Windows. Spazio dei nomi Networking.Proximity.**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Altre risorse**
</dt> <dt>

[Informazioni sul Wi-Fi nativo](about-native-wifi.md)
</dt> <dt>

[Informazioni sull'API Wi-Fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Informazioni sulla Wi-Fi Direct](about-the-wi-fi-direct-api.md)
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

 

 
