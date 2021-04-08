---
title: Novità di Windows Media Player 11
description: In questo argomento vengono elencate le nuove funzionalità di Windows Media Player 11 e Windows Media Player 11 SDK.
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Windows Media Player, novità
- Windows Media Player, nuove funzionalità
- Software Development Kit (SDK), Windows Media Player 11
- SDK (Software Development Kit), Windows Media Player 11
- documentazione, Windows Media Player 11 SDK
- Novità, Windows Media Player 11
- nuove funzionalità, Windows Media Player 11
- interfacce, nuove funzionalità di Windows Media Player 11
- attributi, nuove funzionalità di Windows Media Player 11
- Windows Media Player ActiveX Control, nuove funzionalità della versione 11
- Controllo ActiveX, nuove funzionalità della versione 11
- interfacce, nuove funzionalità di Windows Media Player 11
- Windows Media Player Skin, nuove funzionalità della versione 11
- plug-in, nuove funzionalità di Windows Media Player 11
- Plug-in di Windows Media Player, nuove funzionalità della versione 11
- negozi online, nuove funzionalità di Windows Media Player 11
- Windows Media Player Online Stores, nuove funzionalità della versione 11
- esempi, nuove funzionalità di Windows Media Player 11
- versioni di Windows Media Player, nuove funzionalità della versione 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aa728aa1552ac0e65f5825cad62d8e9e0c7300
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046437"
---
# <a name="what-was-new-in-windows-media-player-11"></a>Novità di Windows Media Player 11

In questo argomento vengono elencate le nuove funzionalità di Windows Media Player 11 e Windows Media Player 11 SDK.

## <a name="windows-media-player-control"></a>Controllo Media Player Windows

Le interfacce seguenti erano nuove nel controllo ActiveX Windows Media Player 11.

-   [**Interfaccia IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interfaccia IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interfaccia IWMPLibrarySharingServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Interfaccia IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interfaccia IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interfaccia IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Mediacollection (oggetto)**](mediacollection-object.md)
-   [**Oggetto query**](query-object.md)
-   [**StringCollection (oggetto)**](stringcollection-object.md)
-   [**Interfaccia IWMPCdromRip**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interfaccia IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interfaccia IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Interfaccia IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Interfaccia IWMPVideoRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**IWMPUserEventSink**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpusereventsink)
-   [**Interfaccia IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)

## <a name="windows-media-player-skins"></a>Interfacce di Media Player Windows

Di seguito sono riportate le nuove funzionalità dell'interfaccia di Windows Media Player 11.

-   Nuovi attributi per il posizionamento dei controlli. Vedere [**AmbientAttributes. Right**](ambientattributes-right.md) e [**AmbientAttributes. Bottom**](ambientattributes-bottom.md).
-   Nuovi attributi per i controlli di ridimensionamento e di trasferimento. Vedere [**AmbientAttributes. moveSizeTo**](ambientattributes-movesizeto.md) e [**AmbientAttributes. slideTo**](ambientattributes-slideto.md).
-   Nuovo attributo per specificare il comportamento di ridimensionamento delle immagini. Vedere [**AmbientAttributes. resizeImages**](ambientattributes-resizeimages.md).
-   Nuovo attributo per specificare il ridimensionamento non uniforme di un elemento Skin. Vedere [**AmbientAttributes. nineGridMargins**](ambientattributes-ninegridmargins.md).

## <a name="windows-media-player-plug-ins"></a>Plug-in di Windows Media Player

In Windows Media Player 11 SDK è stato introdotto un nuovo tipo di plug-in per la conversione di formati di file multimediali digitali. Vedere [plug-in di conversione di Windows Media Player](windows-media-player-conversion-plug-ins.md).

I plug-in DSP creati prima del rilascio di Windows Media Player 11 SDK devono essere aggiornati per funzionare con Windows Media Player 11. Vedere [aggiornamento di plug-in DSP esistenti](updating-existing-dsp-plug-ins.md).

La creazione guidata plug-in di Windows Media Player è stata aggiornata per creare plug-in DSP che funzionano in Windows Media Player 11. Per informazioni dettagliate, vedere [aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

## <a name="windows-media-player-online-stores"></a>Windows Media Player Online Stores

In Windows Media Player 11 è stato introdotto un nuovo modello per l'integrazione dei cataloghi di archivio online nella funzionalità della libreria di Windows Media Player. Vedere gli [archivi online di tipo 1](type-1-online-stores.md).

## <a name="windows-media-player"></a>Windows Media Player

Di seguito sono riportate le nuove funzionalità di Windows Media Player 11.

-   [Estensioni del dispositivo per la creazione di report sul contenuto acquisito](device-extensions-for-reporting-acquired-content.md)
-   [Estensioni dispositivo per preferenze oggetto playlist](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Esempi di Windows Media Player SDK

L'esempio C# denominato SchemaReader è una novità di Windows Media Player 11 SDK. Nell'esempio viene creato uno strumento che utilizza il modello a oggetti di Windows Media Player per recuperare e visualizzare informazioni sui metadati nella libreria Media Player di Windows o in un file multimediale digitale. Lo strumento consente di salvare i risultati in un file di testo. Lo strumento enumera i nomi degli attributi dei metadati archiviati nella libreria per ogni schema supportato (audio, video, playlist, foto e altro). Lo strumento può inoltre fornire informazioni sugli attributi disponibili per le playlist nella raccolta di playlist, le tracce CD, il sommario CD, i titoli DVD, i capitoli DVD, il sommario DVD e i singoli file multimediali.

L'esempio C++ denominato WMPML è stato aggiornato nell'SDK di Windows Media Player 11 per dimostrare le funzionalità seguenti:

-   Uso della nuova interfaccia [**IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) per creare un'interfaccia utente simile alla funzionalità della libreria Media Player di Windows.
-   Uso delle interfacce [**IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) e [**IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) per creare query composte e visualizzare i risultati.

 

 




