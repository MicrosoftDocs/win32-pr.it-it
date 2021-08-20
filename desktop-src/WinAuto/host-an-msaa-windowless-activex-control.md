---
title: Come ospitare un controllo ActiveX msaa
description: Informazioni su come creare un contenitore di controlli in grado di ospitare controlli Microsoft senza ActiveX che implementano Microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, controllo ActiveX finestra
- Controllo ActiveX finestra, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d086fdc33c1b645294827ec62784612ffeb617f12caf5a101ea8472da3e765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115132"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Come ospitare un controllo ActiveX msaa

Informazioni su come creare un contenitore di controlli in grado di ospitare controlli Microsoft senza ActiveX che implementano Microsoft Active Accessibility. Seguendo i passaggi descritti qui, è possibile assicurarsi che tutti i controlli senza finestra basati su Microsoft Active Accessibility ospitati nel contenitore di controlli siano accessibili alle applicazioni client assistive technology (AT).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [ActiveX Controlli](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione Microsoft Win32 e Component Object Model (COM)
-   Controlli ActiveX finestra
-   Microsoft Active Accessibility server

## <a name="instructions"></a>Istruzioni

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Passaggio 1: fornire l'interfaccia IAccessible radice per conto del controllo senza finestra.

Ogni volta che il sistema necessita [**del puntatore IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per la radice di un controllo senza finestra, il sistema esegue una query sul contenitore del controllo. Per recuperare il puntatore, il contenitore chiama l'implementazione del controllo senza finestra [**del metodo IServiceProvider::QueryService.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))

Se il contenitore del controllo Microsoft Active Accessibility un'implementazione di , può restituire al sistema il puntatore [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del controllo senza finestra.

Se il contenitore di controlli ha un'implementazione di Microsoft Automazione interfaccia utente, chiamare la funzione [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) per ottenere un puntatore a interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) che rappresenta il controllo e quindi restituire il puntatore di interfaccia **IRawElementProviderSimple** al sistema.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Passaggio 2: rispondere al messaggio WM \_ GETOBJECT per conto del controllo senza finestra.

Quando un'applicazione client risponde a un WinEvent generato da un controllo senza finestra, il contenitore del controllo riceve un messaggio [**WM \_ GETOBJECT**](wm-getobject.md) per conto del controllo. Il messaggio include l'ID oggetto del controllo senza finestra che ha generato l'evento.

Il contenitore del controllo risponde cercando il controllo senza finestra "proprietario" dell'ID oggetto e quindi chiamando il metodo [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) del controllo. Il **metodo AccessibleObjectFromID** restituisce il puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento dell'interfaccia utente e il contenitore di controlli restituisce il puntatore al sistema, che lo inoltra all'applicazione client.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Passaggio 3: Implementare l'interfaccia IAccessibleWindowlessSite.

1.  Implementare [**il metodo IAccessibleWindowlessSite::GetParentAccessible.**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible)

    Quando un'applicazione client necessita di informazioni di accessibilità sull'elemento padre del provider radice del controllo senza finestra, il sistema chiama il metodo [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del controllo senza finestra. Il controllo risponde chiamando il metodo [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenitore del controllo, che fornisce il puntatore [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'elemento padre del controllo senza finestra.

2.  Implementare [**i metodi IAccessibleWindowlessSite::AcquireObjectIdRange,**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)e [**ReleaseObjectIdRange.**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange)

    Il contenitore di controlli deve mantenere un mapping degli intervalli di ID oggetto ai controlli senza finestra. Il mapping consente al contenitore di controlli di identificare il controllo che deve rispondere a una particolare richiesta di un ID oggetto. La tabella seguente illustra un esempio di mapping degli intervalli di ID oggetto ai controlli senza finestra.

    

    | Base intervallo | Dimensioni intervallo | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Controllo 1 |
    | 1500       | 1000       | Controllo 2 |
    | 2500       | 2000       | Controllo 1 |

    

     

    Il contenitore del controllo deve mantenere il mapping degli intervalli di ID oggetto ai controlli senza finestra per se stesso e per tutti gli elementi figlio senza finestra. Non è necessario che gli intervalli di ID oggetto siano adiacenti l'uno all'altro. Inoltre, per evitare attacchi Denial of Service, il contenitore di controllo può inserire limiti al numero di intervalli concessi a un determinato controllo. Tuttavia, è utile consentire più di un intervallo per ogni controllo, per consentire l'aumentare delle dimensioni di un controllo.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Passaggio 4: Facoltativo: implementare l'interfaccia IAccessibleHostingElementProviders.

Implementare l'interfaccia [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) se il contenitore di controlli ha un'implementazione del server Microsoft Active Accessibility e il server è la radice di un albero di accessibilità che include controlli ActiveX senza finestra che supportano Automazione interfaccia utente. **L'interfaccia IAccessibleHostingElementProviders** ha un unico metodo, [**GetEmbeddedFragmentRoots,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots)che recupera i puntatori all'interfaccia [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) di tutti i controlli ActiveX Automazione interfaccia utente senza finestra ospitati dal contenitore di controlli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come ospitare un controllo Automazione interfaccia utente senza ActiveX finestra](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Accessibilità dei controlli ActiveX finestra](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 