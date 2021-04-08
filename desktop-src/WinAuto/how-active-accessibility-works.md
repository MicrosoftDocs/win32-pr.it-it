---
title: Funzionamento di Active Accessibility
description: Microsoft Active Accessibility è progettato per aiutare gli utenti che facilitano l'accessibilità, chiamati client, a interagire con gli elementi dell'interfaccia utente standard e personalizzati di altre applicazioni e il sistema operativo.
ms.assetid: 29325f0a-c6ca-42b1-b85d-2671f7041034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdeffcebd96ffba804bfc24672bf867028e9b0c7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103857958"
---
# <a name="how-active-accessibility-works"></a>Funzionamento di Active Accessibility

Microsoft Active Accessibility è progettato per aiutare gli utenti che facilitano l'accessibilità, chiamati *client*, a interagire con gli elementi dell'interfaccia utente standard e personalizzati di altre applicazioni e il sistema operativo. Un client di Microsoft Active Accessibility è un programma che utilizza Microsoft Active Accessibility per accedere, identificare o modificare gli elementi dell'interfaccia utente di un'applicazione. I client includono i supporti per l'accessibilità, gli strumenti di test automatizzati e alcune applicazioni di training basate su computer.

Utilizzando Microsoft Active Accessibility, un'applicazione client può:

-   Eseguire una query per ottenere informazioni; ad esempio, su un elemento dell'interfaccia utente in una posizione specifica.
-   Ricevere notifiche in caso di modifica delle informazioni; ad esempio, quando un controllo diventa grigio o quando una stringa di testo viene modificata.
-   Eseguire azioni che interessano l'interfaccia utente o il contenuto del documento; ad esempio, fare clic su un pulsante di push, a discesa di un menu e scegliere un comando di menu.

Le applicazioni che interagiscono con e forniscono informazioni per i client sono denominate *Server*. Un server utilizza Microsoft Active Accessibility per fornire informazioni sugli elementi dell'interfaccia utente ai client. Qualsiasi controllo, modulo o applicazione che utilizza Microsoft Active Accessibility per esporre informazioni sull'interfaccia utente viene considerato un server Microsoft Active Accessibility. I server comunicano con i client inviando notifiche degli eventi, ad esempio chiamando [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), e rispondendo alle richieste dei client per l'accesso agli elementi dell'interfaccia utente (ad esempio la gestione dei messaggi [**WM \_ GetObject**](wm-getobject.md) inviati da [*oleacc*](uiauto-glossary.md)). I server espongono informazioni tramite l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Utilizzando Microsoft Active Accessibility, un'applicazione server può:

-   Fornire informazioni sugli oggetti personalizzati dell'interfaccia utente e sul contenuto delle finestre client.
-   Inviare notifiche quando viene modificata l'interfaccia utente.

Ad esempio, per consentire a un utente di selezionare i comandi in modo verbale da una barra degli strumenti personalizzata del processore di Word, un programma di riconoscimento vocale deve disporre di informazioni su tale barra degli strumenti. Il processore di testo dovrà quindi rendere disponibili tali informazioni. Microsoft Active Accessibility fornisce i mezzi per l'elaboratore di testo per esporre informazioni sulla barra degli strumenti personalizzata e per il programma di riconoscimento vocale per ottenere tali informazioni.

### <a name="client-applications-and-active-accessibility"></a>Applicazioni client e Active Accessibility

Un client di Microsoft Active Accessibility deve ricevere una notifica quando l'interfaccia utente del server è cambiata in modo da poter comunicare tali informazioni all'utente. Per assicurarsi che il client sia informato sulle modifiche dell'interfaccia utente, viene utilizzato un meccanismo denominato eventi finestra, o WinEvents, per la registrazione per la ricezione delle notifiche. Per ulteriori informazioni, vedere [winEvents](winevents-infrastructure.md).

Per conoscere e modificare un particolare elemento dell'interfaccia utente, i client utilizzano l'interfaccia Microsoft Active Accessibility Component Object Model (COM), [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Un client può recuperare un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un elemento dell'interfaccia utente nei quattro modi seguenti:

-   Chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e passare l'handle della finestra dell'elemento dell'interfaccia utente.
-   Chiamare [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) e passare una posizione dello schermo che si trova all'interno del rettangolo di delimitazione dell'elemento dell'interfaccia utente.
-   Impostare un hook WinEvent, ricevere una notifica e chiamare [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) per recuperare un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento dell'interfaccia utente che ha generato l'evento.
-   Chiamare un metodo [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) come [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) o [**get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) per passare a un oggetto **IAccessible** diverso.

 

 




