---
title: Proxy IAccessible
description: I proxy IAccessible forniscono informazioni di accessibilità predefinite per gli elementi dell'interfaccia utente standard controlli UTENTE, menu USER e controlli comuni da COMCTL e COMCTL32.
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a416c29021aca0dd99356792ae96f6a77e137e8c0ca0c884ba941229dd4b83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566056"
---
# <a name="iaccessible-proxies"></a>Proxy IAccessible

I proxy [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) forniscono informazioni di accessibilità predefinite per gli elementi dell'interfaccia utente standard: controlli USER, menu USER e controlli comuni da COMCTL e COMCTL32. Questo supporto predefinito viene esposto tramite **oggetti IAccessible** creati da Oleacc.dll e Microsoft Active Accessibility supporto senza ulteriori attività di sviluppo del server. Il server può quindi usare [l'API](dynamic-annotation-api.md) Di annotazione dinamica per modificare gran parte delle informazioni esposte da Oleacc.dll, ma non ha il controllo completo.

## <a name="creating-a-proxy"></a>Creazione di un proxy

Per determinare se un elemento dell'interfaccia utente supporta in modo nativo [**l'interfaccia IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Oleacc.dll invia un [**messaggio WM \_ GETOBJECT.**](wm-getobject.md) Un valore restituito diverso da zero indica che l'elemento supporta in modo Microsoft Active Accessibility e fornisce il proprio **supporto IAccessible.** Tuttavia, se il valore restituito è zero, Oleacc.dll fornisce un oggetto proxy per l'elemento dell'interfaccia utente e tenta di restituire informazioni significative per suo conto. Per altre informazioni su **WM \_ GETOBJECT,** vedere [Funzionamento di WM \_ GETOBJECT](how-wm-getobject-works.md).

## <a name="what-information-is-exposed"></a>Informazioni esposte

Oleacc.dll usa il nome della classe Windows dell'elemento dell'interfaccia utente per determinare quali informazioni devono essere esposte per ognuna delle relative proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e come raccogliere queste informazioni. Ad esempio, Oleacc.dll chiama la [**funzione GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) per recuperare la proprietà [**Name**](name-property.md) per un pulsante push standard, ma chiama questa stessa funzione per recuperare la proprietà [**Value**](value-property.md) per un controllo di modifica standard. In effetti, Oleacc.dll esegue il mapping di ogni **metodo IAccessible** a un messaggio o a una chiamata di funzione di Microsoft Win32 appropriata o specifica del controllo. Usando questa speciale distinzione tra maiuscole e minuscole basata sul nome della classe, può restituire informazioni significative tramite proxy **IAccessible** senza alcun supporto Microsoft Active Accessibility nel server.

Le applicazioni compilate con elementi dell'interfaccia utente standard ottengono in genere Microsoft Active Accessibility supporto senza attività di sviluppo aggiuntive. Le eccezioni a questa regola sono i controlli che sono stati sottoclassati, che non archiviano le proprie stringhe (assenza dello stile **HASSTRINGS)** o che sono disegnati dal proprietario. In questi casi, Oleacc.dll raccogliere le informazioni necessarie perché le informazioni vengono archiviate all'esterno del controllo. Tuttavia, in molti di questi scenari, le soluzioni alternative stabilite o l'uso dell'annotazione dinamica consentono al server di collaborare con i proxy forniti da Oleacc.dll.

## <a name="generic-proxy-objects"></a>Oggetti proxy generici

Se Oleacc.dll non riconosce il nome della classe dell'elemento dell'interfaccia utente, crea un proxy generico che espone il maggior numero possibile di informazioni. Al massimo, questo include il rettangolo di delimitazione dell'oggetto, l'oggetto padre, il nome (da [**WM \_ GETTEXT)**](/windows/desktop/winmsg/wm-gettext)e tutti gli elementi figlio nella gerarchia della finestra.

 

 