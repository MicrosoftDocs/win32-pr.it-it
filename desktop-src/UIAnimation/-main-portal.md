---
title: Gestione animazioni Windows
description: Gestione animazioni Windows (animazione Windows) consente un'animazione avanzata degli elementi dell'interfaccia utente.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Animazione Windows animazione Windows, portale
- Animazione Windows di gestione animazioni Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963205"
---
# <a name="windows-animation-manager"></a>Gestione animazioni Windows

## <a name="purpose"></a>Scopo

Gestione animazioni Windows (animazione Windows) consente un'animazione avanzata degli elementi dell'interfaccia utente. È progettato per semplificare il processo di aggiunta dell'animazione all'interfaccia utente di un'applicazione e per consentire agli sviluppatori di implementare animazioni uniformi, naturali e interattive.

Il Framework di animazione gestisce la pianificazione e l'esecuzione di animazioni. Fornisce una libreria di funzioni matematiche utili per specificare il comportamento di un elemento dell'interfaccia utente nel tempo e consente inoltre agli sviluppatori di implementare funzioni personalizzate che forniscono comportamenti aggiuntivi.

L'animazione Windows non esegue il rendering. può essere usato con qualsiasi piattaforma grafica, tra cui Direct2D, Direct3D o GDI+.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Guida allo sviluppo di animazioni Windows](windows-animation-developer-guide.md)<br/> | Nella Guida per gli sviluppatori viene fornita una panoramica dell'animazione di Windows e viene fornito codice di esempio che illustra le attività di animazione di base.<br/>          |
| [Informazioni di riferimento sull'animazione Windows](windows-animation-reference.md)<br/>               | Negli argomenti contenuti in questa sezione vengono fornite le specifiche di riferimento per gestione animazioni di Windows.<br/>                           |
| [Esempi di animazioni Windows](windows-animation-samples.md)<br/>                   | Negli argomenti contenuti in questa sezione vengono fornite informazioni dettagliate sugli esempi di codice che supportano la documentazione di Windows Animation Manager. <br/> |
| [Glossario animazione Windows](-ui-animation-glossary.md)<br/>                     | Questo glossario contiene i termini e gli acronimi di interesse per gli sviluppatori che utilizzano Windows Animation Manager.<br/>                               |



 

## <a name="developer-audience"></a>Sviluppatori

L'animazione Windows è progettata per l'uso da parte di sviluppatori C/C++ esperti che hanno familiarità con i concetti COM, di programmazione dell'interfaccia utente e i concetti di animazione generale.

## <a name="run-time-requirements"></a>Requisiti di runtime

Windows Animation Manager è stato introdotto in Windows 7.

Le applicazioni che richiedono il supporto per Windows Animation Manager in Windows Vista possono utilizzare l'aggiornamento della piattaforma per Windows Vista. Le applicazioni che richiedono l'aggiornamento della piattaforma per Windows Vista possono avere Windows Update verificare che sia installato o scaricarlo e installarlo in background in caso contrario. Per ulteriori informazioni, vedere [informazioni sull'aggiornamento della piattaforma per Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Cenni preliminari sull'animazione Windows Scenic](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)
-   [All'interno di Windows 7: Deep Dive and tutorial di Animation Manager](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)
-   [Animazione Windows-argomenti avanzati](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)
-   [Codice di esempio di Windows Animation Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Argomenti correlati

[Cenni preliminari sull'animazione (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)