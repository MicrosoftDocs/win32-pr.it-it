---
description: Ogni monitor può avere la propria profondità di colore.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Colori su più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd799599f3818ad002ee8a0fa1e9478f383b3052dd3a2cc3b8a40843e431b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115321"
---
# <a name="colors-on-multiple-display-monitors"></a>Colori su più monitor di visualizzazione

Ogni monitor può avere la propria profondità di colore. Il sistema regola automaticamente i colori quando le finestre si spostano tra monitor con profondità di colore diverse. In generale, ciò produce buoni risultati. Tuttavia, questo non è sempre ottimale. Per sfruttare le funzionalità di colore di monitor diversi, vedere [la](painting-on-multiple-display-monitors.md) sezione Disegno su più monitor di visualizzazione che segue.

Per determinare se tutti i monitoraggi hanno lo stesso formato di colore, chiamare [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ SAMEDISPLAYFORMAT.

Se il monitor primario è in stato di estrazione, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funzionano come prima, ma su tutti i monitor. Inoltre, vengono sincronizzate le tavolozze di tutti i dispositivi con svasato. Se il monitor principale non è in stato di estrazione, **SelectPalette** e **RealizePalette** selezioneranno la tavolozza sullo sfondo e i dispositivi snodati non verranno sincronizzati.

 

 
