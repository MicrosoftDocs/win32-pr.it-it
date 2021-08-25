---
description: Descrizione dell'uso dell'accessibilità attiva per esporre controlli personalizzati per Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Uso Active Accessibility esporre controlli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d275b6c5639dddfe60f358427751ad4ff4cd7989923dc4a368b3316b3bfc01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934321"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Uso Active Accessibility esporre controlli personalizzati

È possibile usare Microsoft Active Accessibility come modo efficace per rendere i controlli personalizzati compatibili con gli strumenti di accessibilità. Active Accessibility richiede che l'applicazione:

-   Creare Component Object Model (COM) che rappresentano singoli controlli personalizzati o gruppi di controlli che supportano correttamente **l'interfaccia IAccessible.** L'oggetto può essere creato su richiesta quando viene richiesto da un client Active Accessibility.
-   Chiamare [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) quando i controlli vengono creati o distrutti, ottengono o perdono lo stato attivo o cambiano stato.
-   Gestire il messaggio WM \_ GETOBJECT quando viene usato per eseguire query su proprietà dell'oggetto o degli oggetti.

Ai fini di questa discussione, una finestra contenente altri oggetti personalizzati deve essere esposta a Active Accessibility, consentendo al client di individuare e passare agli oggetti figlio. Per altre informazioni su come rendere i controlli personalizzati compatibili con gli strumenti di accessibilità, vedere [Accessibilità.](../accessibility/accessibility.md)

 

 
