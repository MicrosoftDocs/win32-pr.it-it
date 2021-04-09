---
title: Alternative all'annotazione dinamica
description: Alternative all'annotazione dinamica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117994"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternative all'annotazione dinamica

Esistono altri modi per fornire supporto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) personalizzato per gli elementi dell'interfaccia utente e in alcuni casi sono la soluzione corretta. Prima dell'annotazione dinamica, queste tecniche alternative erano le uniche opzioni disponibili per gli sviluppatori. Sono incluse l'implementazione di tutte le tecniche di interfaccia **IAccessible** e a livello di codice.

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implementazione di tutta l'interfaccia IAccessible

Una tecnica alternativa consiste nell'implementare tutte le interfacce [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Questo approccio è spesso necessario per i controlli personalizzati o per gli elementi dell'interfaccia utente radicalmente diversi. Tuttavia, i costi di sviluppo e test sono sufficientemente significativi da evitare, a meno che non sia effettivamente necessario. Se l'obiettivo è modificare una singola proprietà, è difficile giustificare il costo.

## <a name="programmatic-techniques"></a>Tecniche programmatiche

Un'altra opzione consiste nell'usare le tecniche di sottoclasse e di wrapping per modificare le informazioni esposte per una proprietà specifica. Questa è la tecnica che l'annotazione dinamica deve sostituire. Per eseguire l'override di una singola proprietà usando la sottoclasse e il wrapping, lo sviluppatore deve eseguire i passaggi seguenti:

1.  Sottoclasse HWND dell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Intercettare il messaggio [**WM \_ GetObject**](wm-getobject.md) per il valore IParam/ObjID corretto.
3.  Inviare il messaggio [**WM \_ GetObject**](wm-getobject.md) alla classe di base usando la funzione [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) . Se viene restituito zero, chiamare [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); in caso contrario, chiamare [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) sul valore restituito per ottenere il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa del controllo.
4.  Creare una classe wrapper che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ed esegue il wrapping del puntatore all'interfaccia **IAccessible** restituito dal passaggio precedente. Questa classe wrapper Invia tutti i metodi e le proprietà al puntatore all'interfaccia **IAccessible** originale, ad eccezione di quelli che devono essere sottoposti a override. Questa operazione comporta la scrittura di codice di invio per tutte le proprietà e i metodi dell'interfaccia **IAccessible** , indipendentemente dal numero di cui viene effettivamente eseguito l'override.

Inoltre, gli sviluppatori devono verificare le condizioni seguenti:

-   Il metodo o la proprietà sottoposta a override deve gestire solo gli ID figlio richiesti e trasmettere tutti gli altri al puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale.
-   Il wrapping deve anche trasmettere le interfacce [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) e [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) solo se l'oggetto originale lo supporta.
-   Il conteggio dei riferimenti deve essere gestito correttamente, soprattutto se sono supportate altre interfacce.
-   I valori restituiti [**IDispatch**](idispatch-interface.md) devono essere gestiti correttamente, in particolare con il metodo [**ITypeInfo:: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , che deve essere chiamato con un puntatore di interfaccia all'interfaccia wrapper, non un puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) originale.

Queste tecniche richiedono una notevole quantità di lavoro, anche se è necessario eseguire l'override di una o due proprietà. La maggior parte del codice risultante riguarda la creazione di sottoclassi e il wrapping e solo una piccola frazione fornisce effettivamente le informazioni sottoposte a override.

Tuttavia, esistono scenari in cui sono necessarie queste tecniche. Se ad esempio si apportano modifiche strutturali per creare un elemento dell'interfaccia utente segnaposto, è consigliabile usare queste tecniche anziché l'annotazione dinamica.

## <a name="fixing-names-derived-from-labels"></a>Correzione dei nomi derivati dalle etichette

Alcuni controlli comuni di Microsoft Win32, ad esempio il controllo casella di modifica, vengono quasi sempre usati con un'etichetta (una voce LTEXT nel file di risorse) o una casella di gruppo (GROUPBOX nel file di risorse). Microsoft Active Accessibility deriva automaticamente dalla relativa etichetta la proprietà Name del controllo. Per tali controlli, il testo della finestra (visualizzato in Microsoft Visual Studio come nome o proprietà ID) viene ignorato, perché in genere è generato automaticamente e raramente molto descrittivo; ad esempio, "IDC \_ EDIT1".

Se l'interfaccia utente dell'applicazione non è progettata correttamente, Microsoft Active Accessibility potrebbe non essere in grado di impostare correttamente il nome. Per essere associato a un controllo, la casella etichetta o gruppo deve essere posizionata immediatamente prima del controllo dinamico nell'ordine di tabulazione.

È possibile modificare l'ordine di tabulazione usando lo strumento in Visual Studio (dal menu **formato** quando l'editor risorse è aperto) o modificando direttamente il file di risorse.

Nell'esempio seguente viene illustrata la descrizione di un file di risorse di una finestra di dialogo contenente due caselle di modifica con etichetta.


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



In questo esempio le etichette e i controlli non sono elencati nell'ordine di tabulazione corretto. Di conseguenza, Microsoft Active Accessibility assegna il nome "cognome" alla casella di modifica First-Name e nessun nome alla casella di modifica Last-Name.

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



Quando i controlli hanno etichette supplementari, ad esempio per i valori minimo e massimo in un TrackBar, queste etichette devono essere posizionate dopo il controllo nell'ordine di tabulazione. L'etichetta principale del controllo deve apparire immediatamente prima del controllo stesso.

## <a name="naming-controls-without-labels"></a>Denominazione dei controlli senza etichette

Non è sempre possibile o auspicabile avere un'etichetta visibile per ogni controllo. Tuttavia, è comunque possibile specificare un nome per il controllo aggiungendo un'etichetta invisibile. Come sempre, l'etichetta invisibile deve precedere immediatamente il controllo nell'ordine di tabulazione.

Se si usa l'editor di risorse in Microsoft Visual Studio .NET, è possibile impostare la proprietà Visible su false. Per rendere invisibile l'etichetta quando si modifica il file di risorse (RC), aggiungere NOT WS \_ Visible o alla parte Style del controllo Label, come illustrato nell'esempio seguente.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Si noti che qualsiasi tasto di scelta rapida designato funziona anche se l'etichetta è invisibile.

 

 