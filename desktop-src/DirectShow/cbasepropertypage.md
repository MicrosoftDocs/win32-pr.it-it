---
description: La classe CBasePropertyPage è una classe astratta per l'implementazione di una pagina delle proprietà. Utilizzare questa classe se si sta scrivendo un filtro (o un altro oggetto) che supporta le pagine delle proprietà.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Classe CBasePropertyPage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330310"
---
# <a name="cbasepropertypage-class"></a>Classe CBasePropertyPage

![gerarchia di classi cbasepropertypage](images/cprop01.png)

La `CBasePropertyPage` classe è una classe astratta per l'implementazione di una pagina delle proprietà. Utilizzare questa classe se si sta scrivendo un filtro (o un altro oggetto) che supporta le pagine delle proprietà.



| Variabili membro protette                                             | Descrizione                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**\_bDirty m**](cbasepropertypage-m-bdirty.md)                        | Indica se una o più proprietà sono state modificate.                                                                             |
| [**\_DialogId m**](cbasepropertypage-m-dialogid.md)                    | Identificatore di risorsa per la finestra di dialogo.                                                                                               |
| [**m \_ DLG**](cbasepropertypage-m-dlg.md)                              | Handle per la finestra di dialogo.                                                                                                      |
| [**\_HWND m**](cbasepropertypage-m-hwnd.md)                            | Handle per la finestra di dialogo.                                                                                                      |
| [**\_pPageSite m**](cbasepropertypage-m-ppagesite.md)                  | Puntatore all'interfaccia **IPropertyPageSite** del sito della pagina delle proprietà.                                                         |
| [**\_IDQualifica m**](cbasepropertypage-m-titleid.md)                      | Identificatore di risorsa per una stringa che contiene il titolo della finestra di dialogo.                                                                  |
| Metodi pubblici                                                         | Descrizione                                                                                                                       |
| [**CBasePropertyPage**](cbasepropertypage-cbasepropertypage.md)       | Metodo del costruttore.                                                                                                               |
| [**~ CBasePropertyPage**](cbasepropertypage--cbasepropertypage.md)     | Metodo del distruttore. Virtuale.                                                                                                       |
| [**OnActivate**](cbasepropertypage-onactivate.md)                     | Chiamato quando la pagina delle proprietà viene attivata. Virtuale.                                                                              |
| [**OnApplyChanges**](cbasepropertypage-onapplychanges.md)             | Chiamato quando l'utente applica le modifiche alla pagina delle proprietà. Virtuale.                                                               |
| [**OnConnect**](cbasepropertypage-onconnect.md)                       | Fornisce un puntatore **IUnknown** all'oggetto associato alla pagina delle proprietà. Virtuale.                                        |
| [**OnDeactivate**](cbasepropertypage-ondeactivate.md)                 | Chiamato quando viene eliminata definitivamente la finestra di dialogo. Virtuale.                                                                          |
| [**OnDisconnect**](cbasepropertypage-ondisconnect.md)                 | Chiamato quando la pagina delle proprietà deve rilasciare l'oggetto associato. Virtuale.                                                      |
| [**OnReceiveMessage**](cbasepropertypage-onreceivemessage.md)         | Chiamato quando la finestra di dialogo riceve un messaggio. Virtuale.                                                                           |
| Metodi IPropertyPage                                                  | Descrizione                                                                                                                       |
| [**Activate**](cbasepropertypage-activate.md)                         | Crea la finestra di dialogo.                                                                                                    |
| [**Applica**](cbasepropertypage-apply.md)                               | Applica i valori correnti della pagina delle proprietà all'oggetto associato alla pagina delle proprietà.                                          |
| [**Disattivare**](cbasepropertypage-deactivate.md)                     | Elimina definitivamente la finestra di dialogo.                                                                                                       |
| [**GetPageInfo**](cbasepropertypage-getpageinfo.md)                   | Recupera le informazioni sulla pagina delle proprietà.                                                                                    |
| [**Help**](cbasepropertypage-help.md)                                 | Richiama la guida della pagina delle proprietà.                                                                                                   |
| [**IsPageDirty**](cbasepropertypage-ispagedirty.md)                   | Indica se la pagina delle proprietà è stata modificata dopo l'attivazione o dopo la chiamata più recente a **IPropertyPage:: Apply**. |
| [**Spostare**](cbasepropertypage-move.md)                                 | Posiziona e ridimensiona la finestra di dialogo.                                                                                             |
| [**SetObjects**](cbasepropertypage-setobjects.md)                     | Fornisce i puntatori **IUnknown** per gli oggetti associati alla pagina delle proprietà.                                                 |
| [**SetPageSite**](cbasepropertypage-setpagesite.md)                   | Inizializza la pagina delle proprietà.                                                                                                    |
| [**Visualizza**](cbasepropertypage-show.md)                                 | Consente di visualizzare o nascondere la finestra di dialogo.                                                                                                    |
| [**TranslateAccelerator**](cbasepropertypage-translateaccelerator.md) | Indica alla pagina delle proprietà di elaborare una sequenza di tasti.                                                                               |



 

## <a name="remarks"></a>Commenti

Una pagina delle proprietà è un oggetto COM, pertanto è necessario generare un GUID per l'identificatore di classe (CLSID) e fornire una voce nella matrice [**CFactoryTemplate**](cfactorytemplate.md) . Per ulteriori informazioni, vedere [DirectShow e com](directshow-and-com.md). Nell'esempio seguente viene illustrata una voce di class factory tipica:


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



Il filtro deve esporre l'interfaccia **ISpecifyPropertyPages** . Questa interfaccia contiene un solo metodo, **GetPages**, che restituisce il CLSID della pagina delle proprietà. Nell'esempio seguente viene illustrato come implementare questo metodo:


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



Ricordarsi di eseguire l'override anche del metodo **NonDelegatingQueryInterface** del filtro. Per ulteriori informazioni, vedere [DirectShow e com](directshow-and-com.md) e [**INonDelegatingUnknown**](inondelegatingunknown.md).

Successivamente, creare la finestra di dialogo come risorsa nel progetto e creare una risorsa di stringa che contenga il titolo della finestra di dialogo. Entrambi gli ID risorsa sono parametri per il costruttore **CBasePropertyPage** . Mantenere la stringa del titolo in una risorsa rende più semplice la localizzazione della pagina delle proprietà.

La classe **CBasePropertyPage** fornisce un Framework per l'interfaccia **IPropertyPage** . Questo framework chiama diversi metodi virtuali, tra cui [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md)e così via. Nella classe di base, questi metodi restituiscono semplicemente S \_ OK. La classe derivata dovrà eseguire l'override di alcuni o di tutti questi metodi virtuali. Per informazioni dettagliate, vedere la sezione Osservazioni per i singoli metodi.

Per un esempio esteso di come usare questa classe per creare una pagina delle proprietà, vedere [creazione di una pagina delle proprietà di filtro](creating-a-filter-property-page.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




