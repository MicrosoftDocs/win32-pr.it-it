---
description: Descrizione dell'utilizzo di Active Accessibility per esporre i controlli personalizzati per il Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Uso di Active Accessibility per esporre controlli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306724"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Uso di Active Accessibility per esporre controlli personalizzati

È possibile usare Microsoft Active Accessibility come metodo efficace per rendere i controlli personalizzati compatibili con gli strumenti per l'accessibilità. Active Accessibility richiede che l'applicazione:

-   Creare oggetti Component Object Model (COM) che rappresentano singoli controlli o gruppi di controlli personalizzati che supportano correttamente l'interfaccia **IAccessible** . (L'oggetto può essere creato su richiesta quando viene richiesto da un client di Active Accessibility).
-   Chiamare [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) quando i controlli vengono creati o eliminati, ottenere o perdere lo stato attivo o modificare lo stato in altro modo.
-   Gestire il \_ messaggio WM GetObject quando viene usato per eseguire query sulle proprietà dell'oggetto o degli oggetti.

Ai fini di questa discussione, è necessario esporre una finestra contenente altri oggetti personalizzati anche a Active Accessibility, consentendo al client di individuare e spostarsi sugli oggetti figlio. Per altre informazioni su come rendere i controlli personalizzati compatibili con gli strumenti di accessibilità, vedere [accessibilità](../accessibility/accessibility.md).

 

 
