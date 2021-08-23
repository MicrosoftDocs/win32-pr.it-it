---
title: Esposizione di controlli in base ai controlli di sistema
description: Esposizione di controlli in base ai controlli di sistema
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09349819cbc8e36d879947fe0cbd0914a1de630171ef70e3b132f58c60c87228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829098"
---
# <a name="exposing-controls-based-on-system-controls"></a>Esposizione di controlli in base ai controlli di sistema

Prima di provare la tecnica descritta in questa sezione, è consigliabile usare una qualche forma di annotazione dinamica, ovvero diretta, mappa valori o server. Per altre informazioni, vedere [API di annotazione dinamica.](dynamic-annotation-api.md)

Nella maggior parte dei Microsoft Active Accessibility espone informazioni sui controlli superclassati o sottoclassati. La superclasse e la creazione di sottoclassi consentono a uno sviluppatore di applicazioni di creare un controllo personalizzato con le funzionalità di base di un controllo di sistema e di includere i miglioramenti forniti dall'applicazione. Un controllo superclassato ha un nome di classe di finestra diverso rispetto al controllo di sistema su cui è basato. Un controllo sottoclassato ha lo stesso nome di classe della finestra. Per altre informazioni sulla superclasse e la creazione di sottoclassi, vedere la documentazione di Windows Software Development Kit (SDK).

Poiché Microsoft Active Accessibility espone informazioni sui controlli forniti dal sistema, Microsoft Active Accessibility espone il controllo modificato a meno che un controllo superclassato o sottoclassato non sia significativamente diverso dal controllo di base. Per determinare se il controllo modificato è accessibile, gli sviluppatori di applicazioni devono usare utilità come [Inspect](inspect-objects.md) e [Accessible Event Watcher](accessible-event-watcher.md) per confrontare il comportamento del controllo modificato con il controllo di base.

Se dopo aver utilizzato queste utilità si determina che il controllo modificato non è accessibile, è necessario considerare il controllo come qualsiasi altro controllo personalizzato. Il controllo deve attivare eventi e la routine della finestra dell'applicazione deve rispondere al messaggio [**WM \_ GETOBJECT**](wm-getobject.md)fornendo un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) utilizzata dalle applicazioni client per ottenere informazioni sul controllo.

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a>CreateStdAccessibleProxy e CreateStdAccessibleObject

Se tutte o la maggior parte delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per il controllo modificato sono uguali al controllo di base, usare [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) o [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) per semplificare l'implementazione dell'interfaccia **IAccessible** del controllo.

> [!Note]  
> Quando si esegue la superclasse o la creazione di una sottoclasse di un controllo accessibile, tenere presente che l'oggetto recuperato dalla funzione [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) può implementare più di una semplice [**interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Può includere altre interfacce, ad esempio [IEnumVARIANT.](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) Potrebbe essere necessario eseguire il wrapping di queste interfacce aggiuntive per mantenere il supporto dell'accessibilità fornito dall'implementazione originale del controllo.

 

Le [**funzioni CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) e [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) recuperano un puntatore [**a interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per il controllo di sistema specificato. La differenza in queste funzioni è che **CreateStdAccessibleObject** usa il nome della classe della finestra ottenuto dal relativo parametro *hwnd,* mentre **CreateStdAccessibleProxy** usa il nome della classe della finestra specificato nel relativo *parametro szClassName.* Pertanto, se si decide di usare queste funzioni, usare **CreateStdAccessibleProxy** per esporre informazioni sui controlli superclassati e una delle due funzioni con controlli sottoclassati.

Dopo aver ottenuto un [**puntatore di**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfaccia IAccessible al controllo di sistema, usare il puntatore nell'implementazione dell'interfaccia **IAccessible** per il controllo modificato. Se una proprietà o un metodo per il controllo modificato è uguale al controllo di base, usare il puntatore **IAccessible** per restituire le informazioni fornite dal controllo di base. Se una proprietà per il controllo modificato è diversa dal controllo di base, eseguire l'override della proprietà del controllo di base.

Nell'esempio seguente **CAccCustomButton è** la classe definita dall'applicazione derivata da [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) La variabile membro **m \_ pAccDefaultButton** è un puntatore a un'interfaccia **IAccessible** recuperata da [**CreateStdAccessibleObject durante**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) la procedura di inizializzazione per il controllo. In questo esempio la **proprietà Role** per il controllo personalizzato è uguale alla proprietà **Role** del controllo di sistema, quindi viene restituita la proprietà **Role** del controllo di base. Tuttavia, la **proprietà Description** è diversa da quella del controllo di base, pertanto questa proprietà viene sottoposta a override.


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



Per altre informazioni sulle proprietà e i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dei controlli di sistema, vedere [Appendix A: Supported Interfaccia utente Elements Reference](appendix-a--supported-user-interface-elements-reference.md).

 

 