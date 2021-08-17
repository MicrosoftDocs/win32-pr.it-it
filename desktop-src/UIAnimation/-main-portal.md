---
title: Windows Gestione animazione
description: La Windows Animation Manager (Windows Animation) consente l'animazione avanzata degli elementi dell'interfaccia utente.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows Animation Windows Animation ,portal
- Windows Animazione di gestione Windows animazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e6a8f81fbef55525eff04df52a31f8ee942707c354697658ee0ba01647d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755615"
---
# <a name="windows-animation-manager"></a>Windows Gestione animazione

## <a name="purpose"></a>Scopo

La Windows Animation Manager (Windows Animation) consente l'animazione avanzata degli elementi dell'interfaccia utente. È progettato per semplificare il processo di aggiunta dell'animazione all'interfaccia utente di un'applicazione e per consentire agli sviluppatori di implementare animazioni uniformi, naturali e interattive.

Il framework di animazione gestisce la pianificazione e l'esecuzione delle animazioni. Fornisce una libreria di funzioni matematiche utili per specificare il comportamento di un elemento dell'interfaccia utente nel tempo e consente agli sviluppatori di implementare funzioni personalizzate che forniscono comportamenti aggiuntivi.

Windows L'animazione non esegue il rendering; Può essere usato con qualsiasi piattaforma grafica, tra cui Direct2D, Direct3D o GDI+.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Guida allo sviluppo di animazioni](windows-animation-developer-guide.md)<br/> | La guida per gli sviluppatori offre una panoramica dell'Windows e fornisce codice di esempio che illustra le attività di animazione di base.<br/>          |
| [Windows Informazioni di riferimento sulle animazioni](windows-animation-reference.md)<br/>               | Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per Windows Animation Manager.<br/>                           |
| [Windows Esempi di animazione](windows-animation-samples.md)<br/>                   | Gli argomenti contenuti in questa sezione forniscono informazioni dettagliate sugli esempi di codice che supportano la documentazione Windows Animation Manager. <br/> |
| [Windows Glossario dell'animazione](-ui-animation-glossary.md)<br/>                     | Questo glossario contiene termini e acronimi di interesse per gli sviluppatori che usano Windows Animation Manager.<br/>                               |



 

## <a name="developer-audience"></a>Sviluppatori

Windows L'animazione è progettata per l'uso da parte di sviluppatori C/C++ esperti che hanno familiarità con COM, concetti di programmazione dell'interfaccia utente e concetti generali di animazione.

## <a name="run-time-requirements"></a>Requisiti di runtime

Gestione Windows è stato introdotto in Windows 7.

Le applicazioni che richiedono il supporto Windows Animation Manager in Windows Vista possono usare l'aggiornamento della piattaforma per Windows Vista. Le applicazioni che richiedono l'aggiornamento della piattaforma per Windows Vista possono avere Windows Update per verificare che sia installato o scaricarlo e installarlo in background in caso contrario. Per altre informazioni, vedere [Informazioni sull'aggiornamento della piattaforma per Windows Vista.](../win7ip/platform-update-for-windows-vista-overview.md)

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Windows cenni preliminari sull'animazione di Animation Animation](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)
-   [Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (Esercitazione e approfondimenti su Animation Manager) (video)
-   [Windows animation - Argomenti avanzati](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)
-   [Windows Codice di esempio di Animation Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Argomenti correlati

[Cenni preliminari sull'animazione (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)