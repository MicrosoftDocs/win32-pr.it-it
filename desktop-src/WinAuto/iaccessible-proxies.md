---
title: Proxy IAccessible
description: I proxy IAccessible forniscono informazioni di accessibilità predefinite per gli elementi dell'interfaccia utente standard, i menu utente e i controlli comuni da COMCTL e COMCTL32.
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dcb4cae8980e4003d9915c6783e4ddb043a8c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338198"
---
# <a name="iaccessible-proxies"></a>Proxy IAccessible

I proxy [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) forniscono informazioni di accessibilità predefinite per gli elementi dell'interfaccia utente standard: controlli utente, menu utente e controlli comuni da COMCTL e Comctl32. Questo supporto predefinito viene esposto tramite oggetti **IAccessible** creati da Oleacc.dll e fornisce il supporto di Microsoft Active Accessibility senza ulteriori operazioni di sviluppo del server. Il server può quindi usare l' [API di annotazione dinamica](dynamic-annotation-api.md) per modificare la maggior parte delle informazioni esposte da Oleacc.dll, ma non ha il controllo completo.

## <a name="creating-a-proxy"></a>Creazione di un proxy

Per determinare se un elemento dell'interfaccia utente supporta in modo nativo l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , Oleacc.dll Invia un messaggio [**WM \_ GetObject**](wm-getobject.md) . Un valore restituito diverso da zero indica che l'elemento supporta a livello nativo Microsoft Active Accessibility e fornisce il proprio supporto **IAccessible** . Tuttavia, se il valore restituito è zero, Oleacc.dll fornisce un oggetto proxy per l'elemento dell'interfaccia utente e tenta di restituire informazioni significative per suo conto. Per ulteriori informazioni su **WM \_ GetObject**, vedere funzionamento di [WM \_ GetObject](how-wm-getobject-works.md).

## <a name="what-information-is-exposed"></a>Informazioni esposte

Oleacc.dll utilizza il nome della classe di Windows dell'elemento dell'interfaccia utente per determinare quali informazioni devono essere esposte per ciascuna proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e come raccogliere tali informazioni. Ad esempio, Oleacc.dll chiama la funzione [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) per recuperare la proprietà [**Name**](name-property.md) per un pulsante di push standard, ma chiama questa stessa funzione per recuperare la proprietà [**value**](value-property.md) per un controllo di modifica standard. In effetti, Oleacc.dll sta eseguendo il mapping di ogni metodo **IAccessible** a una chiamata di funzione o a un messaggio specifico di Microsoft Win32 o del controllo. Utilizzando questa speciale combinazione di maiuscole e minuscole in base al nome, può restituire informazioni significative tramite proxy **IAccessible** senza alcun supporto Active Accessibility Microsoft nel server.

Le applicazioni compilate con elementi dell'interfaccia utente standard ottengono in genere il supporto completo di Microsoft Active Accessibility senza attività di sviluppo aggiuntive. Le eccezioni a questa regola sono controlli che sono stati sottoclassati, che non archiviano le proprie stringhe (assenza dello stile **HASSTRINGS** ) o che sono disegnate dal proprietario. In questi casi, Oleacc.dll non è in grado di raccogliere le informazioni necessarie perché le informazioni vengono archiviate all'esterno del controllo. Tuttavia, in molti di questi scenari, soluzioni alternative stabilite o l'uso di un'annotazione dinamica, consentono al server di collaborare con i proxy forniti da Oleacc.dll.

## <a name="generic-proxy-objects"></a>Oggetti proxy generici

Se Oleacc.dll non riconosce il nome della classe dell'elemento dell'interfaccia utente, viene creato un proxy generico che espone quante più informazioni possibile. Sono al massimo inclusi il rettangolo di delimitazione dell'oggetto, l'oggetto padre, il nome (da [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)) e gli eventuali elementi figlio nella gerarchia della finestra.

 

 