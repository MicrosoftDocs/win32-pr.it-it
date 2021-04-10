---
title: Elementi dell'interfaccia utente personalizzati
description: Gli sviluppatori di server progettano oggetti accessibili in base all'interfaccia utente di un'applicazione.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855649"
---
# <a name="custom-user-interface-elements"></a>Elementi dell'interfaccia utente personalizzati

Gli sviluppatori di server progettano oggetti accessibili in base all'interfaccia utente di un'applicazione. Poiché [Active Accessibility implementa l'interfaccia IAccessible per conto degli elementi dell'interfaccia utente forniti dal sistema](appendix-a--supported-user-interface-elements-reference.md) , ad esempio caselle di riepilogo, menu e controlli TrackBar, è necessario implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) solo per i tipi seguenti di elementi dell'interfaccia utente personalizzati:

-   Controlli personalizzati creati mediante la registrazione di una classe di finestra definita dall'applicazione
-   Controlli personalizzati disegnati direttamente sullo schermo a cui non è associato un **HWND**
-   Controlli personalizzati, ad esempio i controlli Microsoft ActiveX e Java
-   Controlli o oggetti nella finestra del client dell'applicazione che non sono già esposti

I menu e i controlli creati dal proprietario sono accessibili purché si seguano le linee guida descritte in [collegamenti per esporre gli elementi personalizzati dell'interfaccia utente](shortcuts-for-exposing-custom-user-interface-elements.md). Se si seguono queste linee guida, non è necessario implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per i controlli e i menu creati dal proprietario.

Nella maggior parte dei casi, i controlli sottoclassati e sottoclassati sono accessibili perché il sistema gestisce la funzionalità di base del controllo. Tuttavia, se un controllo sottoclassato o sottoclassato modifica in modo significativo il comportamento del controllo fornito dal sistema su cui si basa, è necessario implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Per altre informazioni, vedere [esposizione di controlli in base ai controlli di sistema](exposing-controls-based-on-system-controls.md).

Se in un'applicazione vengono utilizzati solo elementi dell'interfaccia utente forniti dal sistema, non è necessario implementare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), ad eccezione della relativa finestra client. Ad esempio, un'applicazione che include un editor di testo, non implementato utilizzando un controllo di modifica, espone righe di testo come oggetti accessibili. Si noti che Microsoft Active Accessibility espone automaticamente il testo nei controlli Edit e Rich Edit come una singola stringa di testo nella proprietà [**value**](value-property.md) del controllo.

 

 




