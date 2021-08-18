---
title: Elementi Interfaccia utente personalizzati
description: Gli sviluppatori di server progettano oggetti accessibili in base all'interfaccia utente di un'applicazione.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183a7024f546aa3e982b632430dad88c89ae79082ac3d91da97e56c821fde62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133874"
---
# <a name="custom-user-interface-elements"></a>Elementi Interfaccia utente personalizzati

Gli sviluppatori di server progettano oggetti accessibili in base all'interfaccia utente di un'applicazione. Poiché Active Accessibility implementa [l'interfaccia IAccessible](appendix-a--supported-user-interface-elements-reference.md) per conto di elementi dell'interfaccia utente forniti dal sistema, ad esempio caselle di riepilogo, menu e controlli trackbar, è necessario implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) solo per i tipi seguenti di elementi dell'interfaccia utente personalizzati:

-   Controlli personalizzati creati registrando una classe finestra definita dall'applicazione
-   Controlli personalizzati disegnati direttamente sullo schermo a cui non è associato **un HWND**
-   Controlli personalizzati, ad esempio i controlli Microsoft ActiveX e Java
-   Controlli o oggetti nella finestra client dell'applicazione che non sono già esposti

I menu e i controlli disegnati dal proprietario sono accessibili purché si seguano le linee guida descritte in Collegamenti per [l'esposizione](shortcuts-for-exposing-custom-user-interface-elements.md)di elementi Interfaccia utente personalizzati . Se si seguono queste linee guida, non è necessario implementare [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per i menu e i controlli disegnati dal proprietario.

Nella maggior parte dei casi, i controlli superclassati e sottoclassati sono accessibili perché il sistema gestisce le funzionalità di base del controllo. Tuttavia, se un controllo superclassato o sottoclassato modifica in modo significativo il comportamento del controllo fornito dal sistema su cui è basato, è necessario implementare [**l'interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Per altre informazioni, vedere [Esposizione di controlli basati sui controlli di sistema](exposing-controls-based-on-system-controls.md).

Se un'applicazione usa solo elementi dell'interfaccia utente forniti dal sistema, non è necessario implementare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), ad eccezione della relativa finestra client. Ad esempio, un'applicazione che include un editor di testo, non implementata tramite un controllo di modifica, espone righe di testo come oggetti accessibili. Si noti Microsoft Active Accessibility automaticamente il testo nei controlli di modifica e rich edit come singola stringa di testo nella proprietà [**Value**](value-property.md) del controllo.

 

 




