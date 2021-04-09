---
title: Interfacce (Framework della barra multifunzione)
description: Documentazione di riferimento per le interfacce del Framework della barra multifunzione di Windows.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c168a342b7f362d2d679d578a88011c9d14977
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118866"
---
# <a name="interfaces-ribbon-framework"></a>Interfacce (Framework della barra multifunzione)

Documentazione di riferimento per le interfacce del Framework della barra multifunzione di Windows.

### <a name="interfaces"></a>Interfacce



| Argomento                                                                                  | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | L'interfaccia [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) viene implementata dall'applicazione e definisce i metodi del punto di ingresso di callback per il Framework della barra multifunzione.<br/>                                                                                                                                                                                                              |
| [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | L'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) viene implementata dal framework della barra multifunzione. L'interfaccia **IUICollection** definisce i metodi per modificare dinamicamente i controlli basati su raccolte, ad esempio le varie [raccolte](ribbon-controls-galleries.md) della barra multifunzione e la barra di accesso rapido (QAT), in fase di esecuzione.<br/>                                              |
| [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | L'interfaccia [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) viene implementata dall'applicazione e definisce il metodo necessario per gestire le modifiche apportate a una raccolta in fase di esecuzione.<br/>                                                                                                                                                                                |
| [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | L'interfaccia [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) viene implementata dall'applicazione e definisce i metodi per la raccolta di informazioni sui comandi e la gestione degli eventi di comando dal framework della barra multifunzione.<br/>                                                                                                                                                              |
| [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | L'interfaccia [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)viene implementata dal framework della barra multifunzione e fornisce le funzionalità di base per la visualizzazione [popup del contesto](windowsribbon-controls-contextpopup.md).<br/>                                                                                                                                                                       |
| [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | L'interfaccia [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) viene implementata dal framework della barra multifunzione e definisce i metodi che forniscono le funzionalità di base per il Framework.<br/>                                                                                                                                                                                                     |
| [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | L'interfaccia [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) viene implementata dall'applicazione e definisce il metodo per il recupero di un'immagine da visualizzare nella barra multifunzione e nell'interfaccia utente popup del contesto del Framework della barra multifunzione.<br/>                                                                                                                                                                          |
| [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) è un'interfaccia Factory implementata dal framework della barra multifunzione che definisce il metodo per la creazione di un oggetto [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) .<br/>                                                                                                                                                             |
| [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | L'interfaccia [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) viene implementata dal framework della barra multifunzione e consente di specificare le impostazioni e le proprietà per una barra multifunzione. <br/>                                                                                                                                                                                                               |
| [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)è un'interfaccia di sola lettura che definisce un metodo per il recupero del valore identificato da una chiave della proprietà. Questa interfaccia viene implementata dal framework della barra multifunzione e viene implementata anche dall'applicazione host per ogni elemento dell'oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)di una raccolta di elementi.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento a Windows Ribbon Framework](windowsribbon-reference-entry.md)
</dt> </dl>

 

