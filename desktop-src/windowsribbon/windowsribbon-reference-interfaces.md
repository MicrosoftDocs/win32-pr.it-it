---
title: Interfacce (Ribbon Framework)
description: Documentazione di riferimento per le interfacce Windows framework della barra multifunzione.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e159d66b8eac8501f231e847555823da431e7d1be3417e0fb803f0929be679bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028669"
---
# <a name="interfaces-ribbon-framework"></a>Interfacce (Ribbon Framework)

Documentazione di riferimento per le interfacce Windows framework della barra multifunzione.

### <a name="interfaces"></a>Interfacce



| Argomento                                                                                  | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | [**L'interfaccia IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) viene implementata dall'applicazione e definisce i metodi del punto di ingresso di callback per il framework della barra multifunzione.<br/>                                                                                                                                                                                                              |
| [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | [**L'interfaccia IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) viene implementata dal framework della barra multifunzione. **L'interfaccia IUICollection** definisce i metodi per la modifica dinamica dei controlli basati su raccolta, ad esempio le varie [raccolte](ribbon-controls-galleries.md) della barra multifunzione e la barra di accesso rapido in fase di esecuzione.<br/>                                              |
| [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | [**L'interfaccia IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) viene implementata dall'applicazione e definisce il metodo necessario per gestire le modifiche a una raccolta in fase di esecuzione.<br/>                                                                                                                                                                                |
| [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | [**L'interfaccia IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) viene implementata dall'applicazione e definisce i metodi per raccogliere informazioni sui comandi e gestire gli eventi Command dal framework della barra multifunzione.<br/>                                                                                                                                                              |
| [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | [**L'interfaccia IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)viene implementata dal framework della barra multifunzione e fornisce le funzionalità di base per la [visualizzazione popup di](windowsribbon-controls-contextpopup.md)contesto.<br/>                                                                                                                                                                       |
| [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | [**L'interfaccia IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) viene implementata dal framework della barra multifunzione e definisce i metodi che forniscono le funzionalità di base per il framework.<br/>                                                                                                                                                                                                     |
| [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | [**L'interfaccia IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) viene implementata dall'applicazione e definisce il metodo per recuperare un'immagine da visualizzare nella barra multifunzione e nell'interfaccia utente popup del framework della barra multifunzione.<br/>                                                                                                                                                                          |
| [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**IUIImageFromBitmap è**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) un'interfaccia factory implementata dal framework della barra multifunzione che definisce il metodo per la creazione di un [**oggetto IUIImage.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)<br/>                                                                                                                                                             |
| [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | [**L'interfaccia IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) viene implementata dal framework della barra multifunzione e consente di specificare impostazioni e proprietà per una barra multifunzione. <br/>                                                                                                                                                                                                               |
| [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)è un'interfaccia di sola lettura che definisce un metodo per recuperare il valore identificato da una chiave di proprietà. Questa interfaccia viene implementata dal framework della barra multifunzione e viene implementata anche dall'applicazione host per ogni elemento nell'oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)di una raccolta di elementi.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Informazioni di riferimento sul framework della barra multifunzione](windowsribbon-reference-entry.md)
</dt> </dl>

 

