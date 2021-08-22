---
title: Informazioni sulle versioni del modello a oggetti
description: Informazioni sulle versioni del modello a oggetti
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player,versioni
- Windows Media Player a oggetti, versioni
- modello a oggetti,versioni
- Windows Media Player ActiveX, versioni per il modello a oggetti
- ActiveX, versioni per il modello a oggetti
- Windows Media Player Controllo ActiveX per dispositivi mobili, versioni per il modello a oggetti
- Windows Media Player Mobile, versioni per il modello a oggetti
- versioni di Windows Media Player,modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce90455d93d71f6fde62b97d3b4d38e34963307e60b831c8110a914cc535cffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510061"
---
# <a name="about-the-object-model-versions"></a>Informazioni sulle versioni del modello a oggetti

Windows Media Player 7.0 ha introdotto un nuovo modello a oggetti. Questo modello a oggetti è stato esteso con Windows Media Player 7.1, Windows Media Player per Windows XP, Windows Media Player serie 9, Windows Media Player 10, Windows Media Player 11 e Windows Media Player 12. Ogni argomento in Riferimento al modello a oggetti include una sezione Requisiti che illustra in dettaglio il requisito minimo per la singola proprietà, metodo o evento. Di seguito sono elencati in dettaglio i nuovi oggetti, metodi, proprietà ed eventi aggiunti per ogni versione a partire dalla versione 7.0. Questi elenchi includono anche nuove interfacce, metodi ed eventi C++.

Se un'interfaccia nuova o aggiornata viene esposta anche come oggetto , viene elencato solo l'oggetto . Per individuare l'interfaccia, fare riferimento alle informazioni [di riferimento sul modello a oggetti per C++.](object-model-reference-for-c.md) In genere, è sufficiente aggiungere il prefisso IWMP al nome dell'oggetto. Se una nuova interfaccia estende una esistente, potrebbe essere necessario cercare il numero di versione più recente. Ad esempio, Windows Media Player serie 9 ha introdotto nuove proprietà e metodi disponibili [**dall'oggetto Impostazioni.**](settings-object.md) In C++ sono disponibili tramite [**l'interfaccia IWMPSettings2,**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) che estende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).

## <a name="added-for-windows-media-player-71"></a>Aggiunta per Windows Media Player 7.1

-   [**Proprietà Player.stretchToFit**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Aggiunta per Windows Media Player per Windows XP

-   [**Metodo Controls.step**](controls-step.md)
-   [**Oggetto DVD**](dvd-object.md)
-   [**Proprietà Media.error**](media-error.md)
-   [**Evento Player.DomainChange**](player-player-domainchange.md)
-   [**Evento Player.MediaError**](player-player-mediaerror.md)
-   [**Evento Player.OpenPlaylistSwitch**](player-player-openplaylistswitch.md)
-   [**Proprietà Player.windowlessVideo**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Aggiunta per Windows Media Player serie 9

-   [**Metodo ClosedCaption.getSAMILangID**](closedcaption-getsamilangid.md)
-   [**Metodo ClosedCaption.getSAMILangName**](closedcaption-getsamilangname.md)
-   [**Metodo ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
-   [**Proprietà ClosedCaption.SAMILangCount**](closedcaption-samilangcount.md)
-   [**Proprietà ClosedCaption.SAMIStyleCount**](closedcaption-samistylecount.md)
-   [**Proprietà Controls.audioLanguageCount**](controls-audiolanguagecount.md)
-   [**Proprietà Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
-   [**Proprietà Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
-   [**Proprietà Controls.currentPositionTimecode**](controls-currentpositiontimecode.md)
-   [**Metodo Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
-   [**Metodo Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
-   [**Metodo Controls.getLanguageName**](controls-getlanguagename.md)
-   [**Proprietà ErrorItem.condition**](erroritem-condition.md)
-   [**Proprietà External.appColorLight**](external-appcolorlight.md)
-   [**Evento External.OnColorChange**](external-oncolorchange-event.md)
-   [**Proprietà External.version**](external-version.md)
-   [**Evento IWMPEvents::P layerDockedStateChange**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**Evento IWMPEvents::P layerReconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Evento IWMPEvents::SwitchedToControl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Evento IWMPEvents::SwitchedToPlayerApplication**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**Interfaccia IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**Interfaccia IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**Interfaccia IWMPSkinManager**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Metodo Media.getAttributeCountByType**](media-getattributecountbytype.md)
-   [**Metodo Media.getItemInfoByType**](media-getiteminfobytype.md)
-   [**Oggetto MetadataPicture**](metadatapicture-object.md)
-   [**Oggetto MetadataText**](metadatatext-object.md)
-   [**Evento Player.AudioLanguageChange**](player-player-audiolanguagechange.md)
-   [**Proprietà Player.isRemote**](player-isremote.md)
-   [**Evento Player.MediaCollectionAttributeStringChanged**](player-player-mediacollectionattributestringchanged.md)
-   [**Metodo Player.newMedia**](player-newmedia.md)
-   [**Metodo Player.newPlaylist**](player-newplaylist.md)
-   [**Metodo Player.openPlayer**](player-openplayer.md)
-   [**Proprietà Player.playerApplication**](player-playerapplication.md)
-   [**Evento Player.StatusChange**](player-player-statuschange.md)
-   [**Oggetto PlayerApplication**](playerapplication-object.md)
-   [**Impostazioni.defaultAudioLanguage**](settings-defaultaudiolanguage.md)
-   [**Proprietà Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
-   [**Metodo Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>Aggiunta per Windows Media Player 10

-   [**Interfaccia IWMPGraphCreation**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**Interfaccia IWMPPlayerServices2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**Interfaccia IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**Interfaccia IWMPSyncServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**Enumerazione WMPDeviceStatus**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**Enumerazione WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>Aggiunta per Windows Media Player 11

-   [**Interfaccia IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interfaccia IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
-   [**Interfaccia IWMPCdromRip**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interfaccia IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
-   [**Interfaccia IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**Interfaccia IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Interfaccia IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interfaccia IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
-   [**Interfaccia IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interfaccia IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
-   [**Interfaccia IWMPLibrarySharingServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Interfaccia IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interfaccia IWMPMediaCollection2 (VB e C#)**](iwmpmediacollection2--vb-and-c.md)
-   [**Interfaccia IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interfaccia IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
-   [**Interfaccia IWMPRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**Interfaccia IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Interfaccia IWMPStringCollection2 (VB e C#)**](iwmpstringcollection2--vb-and-c.md)
-   [**Interfaccia IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Interfaccia IWMPVideoRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Oggetto Query**](query-object.md)
-   [**Enumerazione WMPKindFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**Enumerazione WMPKindState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**Enumerazione WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**Enumerazione WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>Aggiunta per Windows Media Player 12

-   [**Interfaccia IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**Interfaccia IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**Interfaccia IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**Interfaccia IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




