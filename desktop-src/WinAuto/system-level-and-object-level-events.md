---
title: Eventi System-Level e Object-Level
description: Microsoft Active Accessibility usa tre classi di WinEvents a livello di sistema, a livello di oggetto e alla console.
ms.assetid: 3333fe6c-38cd-4e7e-be4b-94c9f824e7e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d14a0469527a7654dd3e323adb47d650866ca9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329399"
---
# <a name="system-level-and-object-level-events"></a>Eventi System-Level e Object-Level

Microsoft Active Accessibility usa tre classi di WinEvents: a *livello di sistema*, a livello di *oggetto* e alla *console*. Ogni ha uno dei valori costanti di [evento](event-constants.md) seguenti:

-   Le costanti dell'evento che iniziano con il sistema di eventi \_ identificano gli eventi a livello di sistema. Questi eventi descrivono le situazioni che interessano tutte le applicazioni nel sistema.
-   Le costanti dell'evento che iniziano con l' \_ oggetto evento identificano gli eventi a livello di oggetto. Questi eventi riguardano situazioni specifiche di oggetti all'interno di un'applicazione.
-   Le costanti dell'evento che iniziano con la \_ Console eventi identificano gli eventi a livello di console. Questi eventi indicano le modifiche nelle finestre della console.

Entrambe le classi di eventi di sistema e a livello di oggetto vengono generate dal sistema operativo e dalle applicazioni server. Il sistema operativo genera eventi a livello di sistema e a livello di oggetto per gli scenari seguenti:

-   Notifiche a livello di sistema relative alle modifiche dello stato attivo
-   Modifiche all'attivazione
-   Eventi relativi agli oggetti forniti dal sistema, ad esempio i controlli comuni

Le applicazioni server generano eventi a livello di sistema per oggetti personalizzati che replicano oggetti di sistema, ad esempio menu personalizzati e barre di scorrimento.

Le applicazioni server generano in genere eventi a livello di oggetto per le modifiche agli oggetti accessibili che contengono, ad esempio la creazione, l'eliminazione e la selezione di oggetti.

Sebbene il sistema generi eventi a livello di oggetto per gli oggetti [**finestra**](window.md) , i server devono inviare anche eventi a livello di oggetto per ogni oggetto accessibile contenuto in una finestra. Se, ad esempio, un'applicazione server registra una classe della finestra definita dall'applicazione per creare un controllo personalizzato, il sistema genera eventi a livello di oggetto per la finestra che contiene il controllo personalizzato; il server genera eventi a livello di oggetto per l'oggetto accessibile che fornisce informazioni sul controllo.

I server generano solo eventi a livello di oggetto per i controlli personalizzati per i quali implementano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Per altre informazioni, vedere [elementi personalizzati dell'interfaccia utente](custom-user-interface-elements.md).

 

 




