---
title: Perché usare DirectComposition
description: Questo argomento descrive le funzionalità e i vantaggi di Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Perché usare DirectComposition
- motivi per usare DirectComposition
- Funzionalità e vantaggi di DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9b67b17869c53b393d8a1f1ecb6230a69322d898f691c21370a5b24befda21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562091"
---
# <a name="why-use-directcomposition"></a>Perché usare DirectComposition?

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedi [Modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento descrive le funzionalità e i vantaggi di Microsoft DirectComposition. Contiene le sezioni seguenti:

-   [Creare un'interfaccia utente visivamente coinvolgente](#create-a-visually-engaging-user-interface)
-   [Abilitare animazioni fluide e di grande effetto per l'applicazione](#enable-rich-smooth-animations-for-your-application)
-   [Combinare bitmap da un'ampia gamma di origini](#combine-bitmaps-from-a-variety-of-sources)
-   [Risparmio di memoria grazie all'integrazione con DWM](#memory-savings-though-integration-with-dwm)
-   [Mantenere i dati già presenti](#keep-what-you-already-have)
-   [Argomenti correlati](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a>Creare un'interfaccia utente visivamente coinvolgente

DirectComposition consente di combinare e animare [*gli*](directcomposition-glossary.md) oggetti visivi per creare un'interfaccia utente visivamente coinvolgente per le Windows basate su app. Può essere utile per offrire all'applicazione un aspetto univoco, stabilendo un'identità che la distingue dalle altre applicazioni.

DirectComposition consente anche di semplificare l'uso delle applicazioni. Puoi ad esempio usarlo per creare segnali visivi e transizioni di schermata animate che mostrano le relazioni tra gli elementi sullo schermo.

## <a name="enable-rich-smooth-animations-for-your-application"></a>Abilitare animazioni fluide e di grande effetto per l'applicazione

DirectComposition è un motore di composizione bitmap ad alte prestazioni che usa grafica con accelerazione hardware per ottenere frequenze di fotogrammi elevate, con conseguente panoramica, scorrimento e animazioni uniformi e coerenti di contenuto complesso. Poiché opera su un thread dedicato separato dal thread usato per eseguire il rendering dell'interfaccia utente dell'applicazione, DirectComposition non può mai "affamare" il thread dell'interfaccia utente o interferire con la capacità dell'applicazione di disegnare gli elementi dell'interfaccia utente.

## <a name="combine-bitmaps-from-a-variety-of-sources"></a>Combinare bitmap da un'ampia gamma di origini

Molte Windows basate su modelli hanno un'interfaccia utente costituita da elementi creati da un'ampia gamma di framework di grafica diversi. Ad esempio, un'applicazione potrebbe usare Windows Forms per creare una barra di stato, Windows Graphics Device Interface (GDI) per creare il contenuto della finestra principale, Microsoft DirectX per il contenuto grafico e così via. DirectComposition consente di combinare il contenuto di un'ampia gamma di framework di grafica e di eseguirne il rendering nella stessa finestra di primo livello o figlio senza doversi preoccupare di cosa accade se il contenuto di framework diversi si sovrappone.

## <a name="memory-savings-though-integration-with-dwm"></a>Risparmio di memoria grazie all'integrazione con DWM

Le composizione e le animazioni create da DirectComposition vengono passate a un componente predefinito di Windows denominato [Gestione finestre desktop (DWM)](/windows/desktop/dwm/dwm-overview) per il rendering sullo schermo. Di conseguenza, non sono necessari componenti di rendering speciali o framework dell'interfaccia utente nel computer.

## <a name="keep-what-you-already-have"></a>Mantenere i dati già presenti

Il codice dell'interfaccia utente in un'Windows esistente basata su Windows rappresenta un investimento significativo. Per la maggior parte, DirectComposition consente di comporre e animare il contenuto dell'interfaccia utente esistente. Ciò significa che è possibile usare DirectComposition per apportare aggiornamenti significativi e miglioramenti all'interfaccia utente dell'applicazione senza dover apportare modifiche estese alla codebase dell'interfaccia utente esistente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectComposition](directcomposition-portal.md)
</dt> </dl>

 

 