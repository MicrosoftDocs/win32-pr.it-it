---
title: Informazioni sulle versioni del modello a oggetti
description: Informazioni sulle versioni del modello a oggetti
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player, versioni
- Modello a oggetti di Windows Media Player, versioni
- modello a oggetti, versioni
- Controllo ActiveX di Windows Media Player, versioni per il modello a oggetti
- Controllo ActiveX, versioni per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, versioni per il modello a oggetti
- Windows Media Player Mobile, versioni per il modello a oggetti
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104398751"
---
# <a name="about-the-object-model-versions"></a>Informazioni sulle versioni del modello a oggetti

In Windows Media Player 7,0 è stato introdotto un nuovo modello a oggetti. Questo modello a oggetti è stato esteso con Windows Media Player 7,1, Windows Media Player per Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11 e Windows Media Player 12. Ogni argomento del riferimento del modello a oggetti include una sezione requisiti che descrive in dettaglio il requisito minimo per la singola proprietà, metodo o evento. Negli elenchi seguenti vengono illustrati in dettaglio i nuovi oggetti, i metodi, le proprietà e gli eventi aggiunti per ogni versione a partire dalla versione 7,0. Questi elenchi includono inoltre nuove interfacce, metodi ed eventi di C++.

Quando viene esposta anche un'interfaccia nuova o aggiornata come oggetto, viene elencato solo l'oggetto. Per individuare l'interfaccia, fare riferimento al [riferimento del modello a oggetti per C++](object-model-reference-for-c.md). In genere, sarà sufficiente aggiungere il prefisso IWMP al nome dell'oggetto. Se una nuova interfaccia ne estende una esistente, potrebbe essere necessario cercare il numero di versione più recente. Ad esempio, nella serie Windows Media Player 9 sono stati introdotti nuovi metodi e proprietà disponibili dall'oggetto [**Settings**](settings-object.md) . In C++ sono disponibili tramite l'interfaccia [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , che estende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).

## <a name="added-for-windows-media-player-71"></a>Aggiunta per Windows Media Player 7,1

-   [**Proprietà Player. stretchToFit**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Aggiunta per Windows Media Player per Windows XP

-   [**Metodo Controls. Step**](controls-step.md)
-   [**Oggetto DVD**](dvd-object.md)
-   [**Proprietà media. Error**](media-error.md)
-   [**Evento Player. DomainChange**](player-player-domainchange.md)
-   [**Evento Player. errore MediaError**](player-player-mediaerror.md)
-   [**Evento Player. OpenPlaylistSwitch**](player-player-openplaylistswitch.md)
-   [**Proprietà Player. windowlessVideo**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Aggiunta per la serie Windows Media Player 9

-   [**ClosedCaption. getSAMILangID, metodo**](closedcaption-getsamilangid.md)
-   [**ClosedCaption. getSAMILangName, metodo**](closedcaption-getsamilangname.md)
-   [**ClosedCaption. getSAMIStyleName, metodo**](closedcaption-getsamistylename.md)
-   [**Proprietà ClosedCaption. SAMILangCount**](closedcaption-samilangcount.md)
-   [**Proprietà ClosedCaption. SAMIStyleCount**](closedcaption-samistylecount.md)
-   [**Proprietà Controls. audioLanguageCount**](controls-audiolanguagecount.md)
-   [**Proprietà Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
-   [**Proprietà Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
-   [**Proprietà Controls. currentPositionTimecode**](controls-currentpositiontimecode.md)
-   [**Controls. getAudioLanguageDescription, metodo**](controls-getaudiolanguagedescription.md)
-   [**Controls. getAudioLanguageID, metodo**](controls-getaudiolanguageid.md)
-   [**Controls. getLanguageName, metodo**](controls-getlanguagename.md)
-   [**Proprietà ErrorItem. Condition**](erroritem-condition.md)
-   [**Proprietà External. appColorLight**](external-appcolorlight.md)
-   [**Evento External. OnColorChange**](external-oncolorchange-event.md)
-   [**Proprietà External. Version**](external-version.md)
-   [**IWMPEvents::P evento layerDockedStateChange**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**IWMPEvents::P evento layerReconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Evento IWMPEvents:: SwitchedToControl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Evento IWMPEvents:: SwitchedToPlayerApplication**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**Interfaccia IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**Interfaccia IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**Interfaccia IWMPSkinManager**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Media. getAttributeCountByType, metodo**](media-getattributecountbytype.md)
-   [**Media. getItemInfoByType, metodo**](media-getiteminfobytype.md)
-   [**Oggetto MetadataPicture**](metadatapicture-object.md)
-   [**Oggetto MetadataText**](metadatatext-object.md)
-   [**Evento Player. AudioLanguageChange**](player-player-audiolanguagechange.md)
-   [**Proprietà Player. Remote**](player-isremote.md)
-   [**Evento Player. MediaCollectionAttributeStringChanged**](player-player-mediacollectionattributestringchanged.md)
-   [**Player. newMedia, metodo**](player-newmedia.md)
-   [**Player. nuova playlist, metodo**](player-newplaylist.md)
-   [**Player. openPlayer, metodo**](player-openplayer.md)
-   [**Proprietà Player. playerApplication**](player-playerapplication.md)
-   [**Evento Player. StatusChange**](player-player-statuschange.md)
-   [**Oggetto PlayerApplication**](playerapplication-object.md)
-   [**Proprietà Settings. defaultAudioLanguage**](settings-defaultaudiolanguage.md)
-   [**Proprietà Settings. mediaAccessRights**](settings-mediaaccessrights.md)
-   [**Settings. requestMediaAccessRights, metodo**](settings-requestmediaaccessrights.md)

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
-   [**Oggetto query**](query-object.md)
-   [**Enumerazione WMPBurnFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**Enumerazione WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
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

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




