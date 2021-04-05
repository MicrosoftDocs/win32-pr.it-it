---
title: Come ospitare un controllo ActiveX senza finestra MSAA
description: Informazioni su come creare un contenitore di controlli in grado di ospitare controlli Microsoft ActiveX senza finestra che implementino Microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, controllo ActiveX senza finestra
- Controllo ActiveX senza finestra, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de45313b19490af3c3fffb633f3822ad93d25a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727522"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Come ospitare un controllo ActiveX senza finestra MSAA

Informazioni su come creare un contenitore di controlli in grado di ospitare controlli Microsoft ActiveX senza finestra che implementino Microsoft Active Accessibility. Seguendo i passaggi descritti in questo articolo, è possibile verificare che tutti i controlli privi di finestra basati su Active Accessibility Microsoft ospitati nel contenitore di controllo siano accessibili alle applicazioni client per la tecnologia di Assistive Technology (AT).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli ActiveX](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione Microsoft Win32 e Component Object Model (COM)
-   Controlli ActiveX senza finestra
-   Server Microsoft Active Accessibility

## <a name="instructions"></a>Istruzioni

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Passaggio 1: fornire l'interfaccia IAccessible radice per conto del controllo privo di finestra.

Ogni volta che il sistema necessita del puntatore [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per la radice di un controllo senza finestra, il sistema esegue una query sul contenitore di controlli. Per recuperare il puntatore, il contenitore chiama l'implementazione del controllo senza finestra del metodo [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .

Se il contenitore di controlli ha un'implementazione di Microsoft Active Accessibility, può restituire il puntatore [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del controllo senza finestra al sistema.

Se il contenitore di controlli ha un'implementazione di automazione interfaccia utente Microsoft, chiamare la funzione [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) per ottenere un puntatore a interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) che rappresenta il controllo, quindi restituire il puntatore di interfaccia **IRawElementProviderSimple** al sistema.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Passaggio 2: rispondere al messaggio WM \_ GETobject per conto del controllo privo di finestra.

Quando un'applicazione client risponde a un WinEvent generato da un controllo senza finestra, il contenitore di controlli riceve un messaggio [**WM \_ GetObject**](wm-getobject.md) per conto del controllo. Il messaggio include l'ID oggetto del controllo senza finestra che ha generato l'evento.

Il contenitore di controlli risponde cercando il controllo senza finestra che "possiede" l'ID oggetto, quindi chiamando il metodo [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) del controllo. Il metodo **AccessibleObjectFromID** restituisce il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento dell'interfaccia utente e il contenitore di controlli restituisce il puntatore al sistema, che lo trasmette all'applicazione client.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Passaggio 3: implementare l'interfaccia IAccessibleWindowlessSite.

1.  Implementare il metodo [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) .

    Quando un'applicazione client richiede informazioni sull'accessibilità per l'elemento padre del provider radice del controllo senza finestra, il sistema chiama il metodo [**IAccessible:: Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del controllo senza finestra. Il controllo risponde chiamando il metodo [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenitore di controlli, che fornisce il puntatore [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'elemento padre del controllo senza finestra.

2.  Implementare i metodi [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)e [**ReleaseObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) .

    Il contenitore del controllo deve mantenere un mapping degli intervalli di ID oggetto ai controlli senza finestra. Il mapping consente al contenitore di controlli di identificare il controllo che deve rispondere a una determinata richiesta di un ID oggetto. La tabella seguente illustra un esempio di mapping degli intervalli di ID oggetto ai controlli privi di finestra.

    

    | Base intervallo | Dimensioni intervallo | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Controllo 1 |
    | 1500       | 1000       | Controllo 2 |
    | 2500       | 2000       | Controllo 1 |

    

     

    Il contenitore di controlli deve mantenere il mapping degli intervalli di ID oggetto ai controlli privi di finestra per se stesso e tutti gli elementi figlio senza finestra. Gli intervalli di ID oggetto non devono essere adiacenti tra loro. Inoltre, per evitare gli attacchi Denial of Service, il contenitore di controlli può inserire limiti sul numero di intervalli concessi a un determinato controllo. Tuttavia, è utile consentire più di un intervallo per controllo, per consentire l'aumento delle dimensioni di un controllo.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Passaggio 4: facoltativo: implementare l'interfaccia IAccessibleHostingElementProviders.

Implementare l'interfaccia [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) se il contenitore di controlli ha un'implementazione di Microsoft Active Accessibility server e il server è la radice di un albero di accessibilità che include controlli ActiveX senza finestra che supportano l'automazione interfaccia utente. L'interfaccia **IAccessibleHostingElementProviders** ha un singolo metodo, [**GetEmbeddedFragmentRoots**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots), che recupera i puntatori dell'interfaccia [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) di tutti i controlli ActiveX senza finestra di automazione interfaccia utente ospitati dal contenitore di controlli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come ospitare un controllo ActiveX senza finestra di automazione interfaccia utente](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Accessibilità controllo ActiveX senza finestra](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 