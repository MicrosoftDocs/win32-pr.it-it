---
title: Data binding tramite IPropertyNotifySink
description: Data binding tramite IPropertyNotifySink
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d39c7277d27f0df6c185fc35a926aa98b77b91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714263"
---
# <a name="data-binding-through-ipropertynotifysink"></a>Data binding tramite IPropertyNotifySink

Gli oggetti che supportano le proprietà, ad esempio tramite l'automazione OLE e l'interfaccia **IDispatch** , possono consentire ai client di ricevere notifiche quando determinate proprietà modificano il valore. Tale proprietà viene chiamata proprietà associabile perché le notifiche consentono a un client di sincronizzare la propria visualizzazione dei valori delle proprietà correnti dell'oggetto. Inoltre, è possibile che gli stessi oggetti desiderino consentire a un client di controllare quando è consentita la modifica di determinate proprietà. Tali proprietà sono denominate proprietà di modifica della richiesta.

[**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) è un'interfaccia di notifica standard che supporta proprietà associabili e di modifica richieste. **IPropertyNotifySink** è supportato da un oggetto con proprietà come interfaccia in uscita. Ovvero l'interfaccia stessa viene implementata dall'oggetto sink di un client e il client connette il sink all'oggetto di supporto tramite il meccanismo del punto di connessione descritto in precedenza. **IPropertyNotifySink** è definito come segue:

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

Quando un oggetto desidera notificare ai sink connessi che è stata modificata una proprietà associabile identificata con un DISPID specificato, viene chiamato [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). Se un oggetto modifica contemporaneamente più proprietà, può passare \_ il DISPID Unknown a **OnChanged** nel qual caso un client aggiorna la cache di tutti i valori di proprietà di interesse.

Quando una proprietà di modifica della richiesta sta per essere modificata, un oggetto può chiedere al client se consentirà la modifica. L'oggetto chiama [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) passando il DISPID della proprietà in questione (o DISPID \_ sconosciuto per identificare tutte le proprietà). Il sink del client restituisce \_ OK per indicare che la modifica è consentita, oppure s \_ false (o un errore) per indicare che la modifica non è consentita. Quando un oggetto chiama **OnRequestEdit**, è necessario rispettare i desideri del client attenendosi alla semantica esatta dei \_ valori restituiti S OK e s \_ false.

Si noti che non è possibile usare [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) per la convalida dei dati perché al momento della chiamata il nuovo valore della proprietà non è ancora disponibile. La notifica può essere utilizzata solo per controllare uno stato di sola lettura per una proprietà.

Gli oggetti controllano quali proprietà sono associabili e richiedono modifiche e contrassegnano tali proprietà nelle informazioni sul tipo dell'oggetto. Nelle informazioni sul tipo, l'attributo associabile contrassegna una proprietà come supporto di [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged). L'attributo requestedit contrassegna una proprietà come supporto di [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit).

Una proprietà può supportare entrambi i comportamenti, nel qual caso [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) viene chiamato per primo e solo se la modifica è consentita [**, viene chiamato**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) il metodo.

L'unica eccezione al comportamento di tali proprietà è che non viene inviata alcuna notifica come risultato delle procedure di inizializzazione o caricamento di un oggetto. In questi casi, si presuppone che tutte le proprietà vengano modificate e che tutte siano consentite per la modifica. Le notifiche a questa interfaccia sono pertanto significative solo nel contesto di un oggetto completamente inizializzato/caricato.

È possibile applicare altri due attributi alle proprietà nelle informazioni sul tipo di un oggetto. L'attributo defaultbind contrassegna una proprietà associabile come quella che meglio rappresenta lo stato dell'oggetto nel suo complesso. L'attributo DisplayBind contrassegna una proprietà associabile come adatta per la visualizzazione nell'interfaccia utente di un client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pagine delle proprietà e finestre delle proprietà](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




