---
title: Alternative all'annotazione dinamica
description: Alternative all'annotazione dinamica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af7582ec0fa3f317a0fabbdde0474c6a2e4d0b361062243d7518edf317477ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122431"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternative all'annotazione dinamica

Esistono altri modi per fornire il supporto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) personalizzato per gli elementi dell'interfaccia utente e in alcuni casi sono la soluzione corretta. Prima dell'annotazione dinamica, queste tecniche alternative erano le uniche opzioni disponibili per gli sviluppatori. Includono l'implementazione di tutte le tecniche a livello di codice e dell'interfaccia **IAccessible.**

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implementazione di tutta l'interfaccia IAccessible

Una tecnica alternativa consiste nell'implementare tutta [**l'interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Questo approccio è spesso necessario per controlli personalizzati o elementi dell'interfaccia utente radicalmente diversi. Tuttavia, i costi di sviluppo e test sono sufficientemente significativi da essere evitati a meno che non siano realmente necessari. Se l'obiettivo è modificare una singola proprietà, il costo è difficile da giustificare.

## <a name="programmatic-techniques"></a>Tecniche a livello di codice

Un'altra opzione consiste nell'usare le tecniche di sottoclassazione e wrapping per modificare le informazioni esposte per una proprietà specifica. Questa è la tecnica che l'annotazione dinamica deve sostituire. Per eseguire l'override di una singola proprietà usando la sottoclassazione e il wrapping, lo sviluppatore deve eseguire la procedura seguente:

1.  Sottoclasse HWND [**dell'oggetto IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
2.  Intercettare [**il messaggio WM \_ GETOBJECT**](wm-getobject.md) per il valore IParam/OBJID corretto.
3.  Inoltrare [**il messaggio WM \_ GETOBJECT**](wm-getobject.md) alla classe di base usando la [*funzione CallWndProc.*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) Se viene restituito zero, chiamare [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject). In caso contrario, chiamare [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) sul valore restituito per ottenere il puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo del controllo.
4.  Creare una classe wrapper, che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ed esegue il wrapping del puntatore a interfaccia **IAccessible** restituito dal passaggio precedente. Questa classe wrapper invia tutti i metodi e le proprietà al puntatore a interfaccia **IAccessible** originale, ad eccezione di quelli di cui eseguire l'override. Ciò comporta la scrittura di codice di inoltro per tutte le 21 proprietà e metodi dell'interfaccia **IAccessible,** indipendentemente dal numero effettivamente sottoposto a override.

Inoltre, gli sviluppatori devono verificare le condizioni seguenti:

-   Il metodo o la proprietà sottoposta a override deve gestire solo gli ID figlio necessari e inoltrare tutti gli altri al puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale.
-   Il wrapping deve anche inoltrare le interfacce [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) e [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) solo se l'oggetto originale le supporta.
-   Il conteggio dei riferimenti deve essere gestito correttamente, soprattutto se sono supportate altre interfacce.
-   I valori restituiti [**IDispatch**](idispatch-interface.md) devono essere gestiti correttamente, in particolare con il metodo [**ITypeInfo::Invoke,**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) che deve essere chiamato con un puntatore a interfaccia all'interfaccia wrapper, non con un puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale.

Queste tecniche richiedono una notevole quantità di lavoro, anche se è necessario eseguire l'override di una o due proprietà. La maggior parte del codice risultante riguarda la sottoclasse e il wrapping e solo una piccola frazione fornisce effettivamente le informazioni sottoposte a override.

Esistono tuttavia scenari in cui queste tecniche sono necessarie. Ad esempio, se si apportano modifiche strutturali per creare un elemento segnaposto dell'interfaccia utente, è consigliabile usare queste tecniche anziché l'annotazione dinamica.

## <a name="fixing-names-derived-from-labels"></a>Correzione dei nomi derivati dalle etichette

Alcuni controlli comuni di Microsoft Win32, ad esempio il controllo casella di modifica, vengono quasi sempre usati con un'etichetta (una voce LTEXT nel file di risorse) o una casella di gruppo (GROUPBOX nel file di risorse). Microsoft Active Accessibility deriva automaticamente la proprietà name del controllo dalla relativa etichetta. Per tali controlli, il testo della finestra (visualizzato Microsoft Visual Studio come proprietà Name o ID) viene ignorato, perché in genere viene rigenerato automaticamente e raramente molto descrittivo. ad esempio "IDC \_ EDIT1".

Se l'interfaccia utente dell'applicazione non è progettata correttamente, Microsoft Active Accessibility potrebbe non essere possibile impostare correttamente il nome. Per essere associata a un controllo, l'etichetta o la casella di gruppo deve essere posizionata immediatamente prima del controllo dinamico nell'ordine di tabulazione.

L'ordine di tabulazione può essere modificato usando lo strumento in Visual Studio **(nel** menu Formato quando l'editor di risorse è aperto) o modificando direttamente il file di risorse.

L'esempio seguente illustra la descrizione di un file di risorse di una finestra di dialogo che contiene due caselle di modifica etichettate.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



In questo esempio le etichette e i controlli non sono elencati nell'ordine di tabulazione corretto. Di conseguenza, Microsoft Active Accessibility assegna il nome "Cognome" alla casella di modifica del nome e nessun nome alla casella di modifica del cognome.

Nell'esempio seguente viene illustrato l'elenco di risorse corretto. Si noti anche che i tasti di scelta rapida sono stati designati nelle etichette.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



Quando i controlli hanno etichette supplementari, ad esempio per i valori minimo e massimo in un trackbar, queste etichette devono essere posizionate dopo il controllo nell'ordine di tabulazione. L'etichetta principale del controllo deve essere visualizzata immediatamente prima del controllo stesso.

## <a name="naming-controls-without-labels"></a>Denominazione di controlli senza etichette

Non è sempre possibile o auspicabile avere un'etichetta visibile per ogni controllo. Tuttavia, è comunque possibile specificare un nome per il controllo aggiungendo un'etichetta invisibile. Come sempre, l'etichetta invisibile deve precedere immediatamente il controllo nell'ordine di tabulazione.

Se si usa l'Editor risorse in Microsoft Visual Studio .NET, è possibile impostare la proprietà Visible su False. Per rendere invisibile l'etichetta durante la modifica del file di risorse (RC), aggiungere NOT WS VISIBLE o alla parte di stile del controllo etichetta, come illustrato \_ nell'esempio seguente.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Si noti che qualsiasi tasto di scelta rapida designato funziona anche se l'etichetta è invisibile.

 

 