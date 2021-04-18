---
title: Esposizione di controlli in base ai controlli di sistema
description: Esposizione di controlli in base ai controlli di sistema
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399487"
---
# <a name="exposing-controls-based-on-system-controls"></a>Esposizione di controlli in base ai controlli di sistema

È consigliabile prendere in considerazione l'uso di una forma di annotazione dinamica, ovvero diretta, mappa di valori o server, prima di provare la tecnica descritta in questa sezione. Per altre informazioni, vedere [API di annotazione dinamica](dynamic-annotation-api.md).

Nella maggior parte dei casi, Microsoft Active Accessibility espone informazioni sui controlli sottoclassati o sottoclassati. La superclasse e la creazione di sottoclassi consentono a uno sviluppatore di applicazioni di creare un controllo personalizzato con la funzionalità di base di un controllo del sistema e includere i miglioramenti forniti dall'applicazione. Un controllo con superclasse ha un nome di classe di finestra diverso dal controllo del sistema su cui si basa. Un controllo sottoclassato ha lo stesso nome della classe di finestra. Per ulteriori informazioni sulla superclasse e la creazione di sottoclassi, vedere la documentazione di Windows Software Development Kit (SDK).

Poiché Microsoft Active Accessibility espone informazioni sui controlli forniti dal sistema, Microsoft Active Accessibility espone il controllo modificato a meno che un controllo sottoclassato o sottoclassato sia significativamente diverso dal controllo di base. Per determinare se il controllo modificato è accessibile, gli sviluppatori di applicazioni devono utilizzare utilità quali [ispezione](inspect-objects.md) e [monitoraggio eventi accessibile](accessible-event-watcher.md) per confrontare il comportamento del controllo modificato con il controllo di base.

Se dopo l'utilizzo di queste utilità si stabilisce che il controllo modificato non è accessibile, è necessario considerare il controllo come qualsiasi altro controllo personalizzato. Il controllo deve attivare gli eventi e la routine della finestra dell'applicazione deve rispondere al messaggio [**WM \_ GetObject**](wm-getobject.md)fornendo un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) utilizzata dalle applicazioni client per ottenere informazioni sul controllo.

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a>CreateStdAccessibleProxy e CreateStdAccessibleObject

Se tutte o la maggior parte delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per il controllo modificato sono le stesse del controllo di base, utilizzare [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) o [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) per semplificare l'implementazione dell'interfaccia **IAccessible** del controllo.

> [!Note]  
> Quando si esegue la superclasse o si crea una sottoclasse di un controllo accessibile, tenere presente che l'oggetto recuperato dalla funzione [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) può implementare solo l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Potrebbe includere altre interfacce, ad esempio [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant). Potrebbe essere necessario eseguire il wrapping di queste interfacce aggiuntive per mantenere il supporto per l'accessibilità fornito dalla implementazione originale del controllo.

 

Le funzioni [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) e [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) recuperano un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per il controllo di sistema specificato. La differenza in queste funzioni è che **CreateStdAccessibleObject** usa il nome della classe di finestra ottenuto dal parametro *HWND* , mentre **CreateStdAccessibleProxy** usa il nome della classe di finestra specificato nel parametro *szClassName* . Se pertanto si decide di usare queste funzioni, usare **CreateStdAccessibleProxy** per esporre le informazioni sui controlli con superclasse e una funzione con controlli sottoclassati.

Dopo avere ottenuto un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) al controllo di sistema, utilizzare il puntatore nell'implementazione dell'interfaccia **IAccessible** per il controllo modificato. Se una proprietà o un metodo per il controllo modificato corrisponde al controllo di base, utilizzare il puntatore **IAccessible** per restituire le informazioni fornite dal controllo di base. Se una proprietà per il controllo modificato è diversa dal controllo di base, eseguire l'override della proprietà del controllo di base.

Nell'esempio seguente **CAccCustomButton** è la classe definita dall'applicazione derivata da [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). La variabile membro **m \_ pAccDefaultButton** è un puntatore a un'interfaccia **IAccessible** che è stata recuperata da [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) durante la procedura di inizializzazione per il controllo. In questo esempio, la proprietà **Role** per il controllo personalizzato corrisponde alla proprietà **Role** del controllo di sistema, pertanto viene restituita la proprietà **Role** del controllo di base. Tuttavia, la proprietà **Description** è diversa da quella del controllo di base, quindi questa proprietà viene sottoposta a override.


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



Per ulteriori informazioni sulle proprietà e sui metodi di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dei controlli di sistema, vedere [Appendice A: riferimenti agli elementi dell'interfaccia utente supportati](appendix-a--supported-user-interface-elements-reference.md).

 

 