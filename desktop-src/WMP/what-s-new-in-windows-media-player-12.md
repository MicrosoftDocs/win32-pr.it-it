---
title: Novità di Windows Media Player 12
description: In questo argomento vengono elencate le nuove funzionalità di Windows Media Player 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player, novità
- Windows Media Player, nuove funzionalità
- Software Development Kit (SDK), Windows Media Player 12
- SDK (Software Development Kit), Windows Media Player 12
- documentazione, Windows Media Player 12 SDK
- Novità, Windows Media Player 12
- nuove funzionalità, Windows Media Player 12
- interfacce, nuove funzionalità di Windows Media Player 12
- attributi, nuove funzionalità di Windows Media Player 12
- metadati, nuove funzionalità di Windows Media Player 12
- enumerazioni, nuove funzionalità di Windows Media Player 12
- flag, nuove funzionalità di Windows Media Player 12
- interfacce, deprecate in Windows Media Player 12
- metodi, deprecati in Windows Media Player 11 e non 12
- versioni di Windows Media Player, nuove funzionalità della versione 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104117482"
---
# <a name="whats-new-in-windows-media-player-12"></a>Novità di Windows Media Player 12

In questo argomento vengono elencate le nuove funzionalità di Windows Media Player 12.

## <a name="new-interfaces"></a>Nuove interfacce

-   [**IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>Nuovi attributi

I nuovi attributi seguenti per gli elementi multimediali sono disponibili tramite le interfacce [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) e [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .

-   [**AlbumCoverURL**](wm-albumcoverurl-attribute.md)
-   [**AlternateSourceURL**](alternatesourceurl-attribute.md)
-   [**DLNASourceURI**](dlnasourceuri-attribute.md)
-   [**DLNAServerUDN**](dlnaserverudn-attribute.md)
-   [**DTCPIPHost**](dtcpiphost-attribute.md)
-   [**DTCPIPPort**](dtcpipport-attribute.md)
-   [**IDLibreria**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>Nuovi metadati del dispositivo

I nuovi elementi di metadati del dispositivo seguenti possono essere recuperati chiamando [**IWMPSyncDevice:: GetItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).

-   **BackgroundSyncState**
-   **SkippedFiles**
-   **SyncFilter**

I nuovi elementi di metadati del dispositivo seguenti possono essere impostati chiamando [**IWMPSyncDevice2:: setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).

-   **AutoSyncDefaultRules**
-   **BackgroundSyncState**
-   **IncludeSkippedFiles**
-   **SyncFilter**
-   **SyncOnConnect**

## <a name="new-enumeration-member"></a>Nuovo membro di enumerazione

L'enumerazione [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) dispone del nuovo membro seguente.

-   **wmpssEstimating**

## <a name="new-flag"></a>Nuovo flag

Il metodo [**IWMPGraphCreation:: GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) supporta il seguente nuovo flag.

-   **\_flag WMPGC \_ usare \_ un \_ grafo personalizzato**

## <a name="deprecated-interface"></a>Interfaccia deprecata

L'interfaccia seguente è deprecata.

-   [**IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>Metodi che non sono più deprecati

I metodi seguenti sono stati deprecati in Windows Media Player 11 SDK, ma non sono più deprecati.

-   [**IWMPGraphCreation::GraphCreationPreRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**IWMPGraphCreation::GraphCreationPostRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Windows Media Player SDK](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




