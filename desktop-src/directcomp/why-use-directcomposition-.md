---
title: Perché usare DirectComposition
description: In questo argomento vengono descritte le funzionalità e i vantaggi di Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Perché usare DirectComposition
- motivi per usare DirectComposition
- Funzionalità e vantaggi di DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300304"
---
# <a name="why-use-directcomposition"></a>Perché usare DirectComposition?

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

In questo argomento vengono descritte le funzionalità e i vantaggi di Microsoft DirectComposition. Contiene le sezioni seguenti:

-   [Creare un'interfaccia utente visivamente accattivante](#create-a-visually-engaging-user-interface)
-   [Abilita animazioni complete e uniformi per l'applicazione](#enable-rich-smooth-animations-for-your-application)
-   [Combinare bitmap da un'ampia gamma di origini](#combine-bitmaps-from-a-variety-of-sources)
-   [Risparmio di memoria tramite l'integrazione con DWM](#memory-savings-though-integration-with-dwm)
-   [Mantieni gli elementi già disponibili](#keep-what-you-already-have)
-   [Argomenti correlati](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Creare un'interfaccia utente visivamente accattivante

DirectComposition consente di combinare e animare gli oggetti [*visivi*](directcomposition-glossary.md) per creare un'interfaccia utente visivamente accattivante per le applicazioni basate su Windows. Può aiutare a offrire all'applicazione un aspetto univoco, definendo un'identità che la distingue dalle altre applicazioni.

DirectComposition può anche semplificare l'uso delle applicazioni. Puoi ad esempio usarlo per creare segnali visivi e transizioni di schermata animate che mostrano le relazioni tra gli elementi sullo schermo.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Abilita animazioni complete e uniformi per l'applicazione

DirectComposition è un motore di composizione bitmap a prestazioni elevate che usa grafica con accelerazione hardware per ottenere frequenze di fotogrammi elevate, ottenendo una panoramica uniforme e coerente, uno scorrimento e animazioni di contenuto complesso. Poiché opera su un thread dedicato separato dal thread usato per il rendering dell'interfaccia utente dell'applicazione, DirectComposition non può mai "affamare" il thread dell'interfaccia utente o interferire con la capacità dell'applicazione di disegnare gli elementi dell'interfaccia utente.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Combinare bitmap da un'ampia gamma di origini

Molte applicazioni basate su Windows hanno un'interfaccia utente costituita da elementi creati da un'ampia gamma di Framework di grafica diversi. Ad esempio, un'applicazione può utilizzare Windows Form per creare una barra di stato, Windows Graphics Device Interface (GDI) per creare il contenuto della finestra principale, Microsoft DirectX per il contenuto grafico e così via. DirectComposition consente di combinare il contenuto di un'ampia gamma di Framework di grafica e di eseguirne il rendering nella stessa finestra di primo livello o figlio senza doversi preoccupare di ciò che accade se il contenuto di Framework diversi si sovrappone.

## <a name="memory-savings-though-integration-with-dwm"></a>Risparmio di memoria tramite l'integrazione con DWM

Le composizioni e le animazioni create da DirectComposition vengono passate a un componente incorporato di Windows denominato [Gestione finestre desktop (DWM)](/windows/desktop/dwm/dwm-overview) per il rendering sullo schermo. Non sono pertanto necessari particolari componenti di rendering o Framework dell'interfaccia utente nel computer.

## <a name="keep-what-you-already-have"></a>Mantieni gli elementi già disponibili

Il codice dell'interfaccia utente in un'applicazione esistente basata su Windows rappresenta un investimento significativo. Nella maggior parte dei casi, DirectComposition consente di comporre e animare il contenuto dell'interfaccia utente esistente. Ciò significa che è possibile usare DirectComposition per apportare aggiornamenti significativi e miglioramenti all'interfaccia utente dell'applicazione senza dover apportare modifiche estese alla base di codice dell'interfaccia utente esistente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 