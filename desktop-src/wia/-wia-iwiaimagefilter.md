---
description: L'interfaccia IWiaImageFilter è un'interfaccia di estensione implementata dagli sviluppatori di filtri di elaborazione immagini e chiamata da Windows Image Acquisition (WIA) 2.0.
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: Interfaccia IWiaImageFilter (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: d7c85a25d7478e0ad51a1d427e74b69a743bc4203ed57b8929a3e4ec856d94b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813981"
---
# <a name="iwiaimagefilter-interface"></a>Interfaccia IWiaImageFilter

**L'interfaccia IWiaImageFilter** è un'interfaccia di estensione implementata dagli sviluppatori di filtri di elaborazione immagini e chiamata da Windows Image Acquisition (WIA) 2.0.

## <a name="members"></a>Membri

**L'interfaccia IWiaImageFilter** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaImageFilter** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWiaImageFilter.**



| Metodo                                                                | Descrizione                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ApplyProperties**](-wia-iwiaimagefilter-applyproperties.md)       | Consente al filtro di elaborazione delle immagini di scrivere di nuovo le proprietà nel driver (e nel dispositivo).<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | Filtra l'immagine di anteprima.<br/>                                                                   |
| [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)     | Inizializza il filtro. Chiamato da WIA 2.0 prima del download di ogni immagine. <br/>                       |
| [**SetNewCallback**](-wia-iwiaimagefilter-setnewcallback.md)         | Imposta un nuovo callback dell'applicazione per il filtro di elaborazione delle immagini da usare per l'inoltro delle chiamate.<br/> |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori di filtri di elaborazione delle immagini devono implementare questa interfaccia e [**l'interfaccia IWiaTransferCallback.**](-wia-iwiatransfercallback.md)

WIA 2.0 chiama i metodi di filtro. Non vengono mai chiamate direttamente da un'applicazione.

Microsoft fornisce il componente di anteprima di WIA 2.0, che memorizza nella cache l'immagine di anteprima originale non filtrata acquisita dallo scanner. Un'applicazione usa [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare insieme un'istanza del componente di anteprima di WIA 2.0 (CLSID WiaPreview), che carica il filtro \_ [**usando IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md). Il filtro viene chiamato automaticamente quando l'applicazione chiama [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md).

Il filtro di elaborazione delle immagini viene sempre eseguito quando un'immagine viene analizzata. Un'applicazione non può acquisire un'immagine dallo scanner senza che il filtro di creazione immagini sia stato applicato per primo.

Un filtro deve implementare almeno luminosità e contrasto. L'interfaccia utente comune, che fornisce controlli di luminosità e contrasto all'utente, può visualizzare anteprime accurate per l'utente.

Un filtro di elaborazione delle immagini non deve mai modificare il membro *lMessage* della [**struttura WiaTransferParams.**](-wia-wiatransferparams.md)

Per leggere le proprietà necessarie, il filtro di elaborazione delle immagini deve chiamare [**IWiaPropertyStorage::GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) [**sull'interfaccia IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) che ottiene dall'elemento chiamando [IWiaImageFilter::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Il filtro può quindi creare [un'istanza di IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) in questo flusso per leggere le proprietà degli elementi. Il filtro di elaborazione delle immagini non deve chiamare [direttamente IWiaPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) perché questo metodo chiama nell'oggetto del driver , ma il servizio WIA 2.0 ha già bloccato il driver nella chiamata, pertanto questa chiamata avrà `drvReadItemProperties` `drvAcquireItemData` esito negativo e timeout.

Le proprietà a cui è interessato il filtro possono essere, ad esempio, le impostazioni di luminosità e contrasto. Il filtro in genere deve anche leggere il formato dell'immagine e la proprietà di anteprima, [**WIA \_ DPS \_ PREVIEW,**](-wia-wiaitempropscannerdevice.md)da *pWiaItem2*. Queste proprietà vengono tutte usate nel processo di filtro.

I componenti di WIA 2.0 scrive sempre dati non filtrati nel filtro di elaborazione delle immagini. L'algoritmo di elaborazione delle immagini implementato dal flusso del filtro può filtrare i dati più di una volta e non deve preoccuparsi di produrre gli stessi risultati del filtro dei dati una sola volta.

Il filtro deve prestare attenzione alla proprietà [**WIA \_ DPS \_ PREVIEW,**](-wia-wiaitempropscannerdevice.md) soprattutto se alcune attività correlate al filtro vengono gestite nell'hardware. Ad esempio, un determinato driver può modificare la luminosità della lampadina nell'hardware dello scanner a seconda di come l'applicazione ha impostato la luminosità in un elemento WIA 2.0. Durante l'analisi finale (quando l'applicazione chiama [**IWiaTransfer::D ownload)**](-wia-iwiatransfer-download.md)il driver modifica in genere la lampadina fisica dello scanner. In questo caso, il filtro di elaborazione delle immagini potrebbe non essere necessario eseguire alcuna elaborazione della luminosità. Durante un'analisi di anteprima, tuttavia, il driver non deve modificare la luminosità della lampadina, ma deve essere presa in considerazione solo nel filtro di elaborazione delle immagini. È importante che il componente di anteprima di WIA 2.0 e il filtro di elaborazione delle immagini restituiranno immagini accurate in base alle proprietà impostate nell'elemento.

Un filtro di elaborazione delle immagini deve supportare tutti i formati di immagine supportati dal driver.

Al filtro di elaborazione delle immagini viene sempre data un'immagine corrispondente all'area di selezione impostata nell'elemento per cui si sta acquisendo l'immagine. Si noti, tuttavia, che l'immagine potrebbe essere stata ruotata dal driver nel caso in cui supporti la proprietà [**\_ WIA IPS \_ ROTATION.**](-wia-wiaitempropscanneritem.md)

Il filtro di elaborazione delle immagini viene creato tramite [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md), in genere non dall'applicazione, ma dai componenti WIA 2.0 quando un'applicazione chiama [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) o [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md).

**L'interfaccia IWiaImageFilter,** come tutte le Component Object Model (COM), eredita i [metodi dell'interfaccia IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
