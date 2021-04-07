---
description: L'interfaccia IWiaImageFilter è un'interfaccia di estensione implementata dagli sviluppatori di filtri per l'elaborazione di immagini e chiamata da Windows Image Acquisition (WIA) 2,0.
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: Interfaccia IWiaImageFilter (WIA. h)
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
ms.openlocfilehash: 8d859b79d15db627bb09cb60f758791a8b5860f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881885"
---
# <a name="iwiaimagefilter-interface"></a>Interfaccia IWiaImageFilter

L'interfaccia **IWiaImageFilter** è un'interfaccia di estensione implementata dagli sviluppatori di filtri per l'elaborazione di immagini e chiamata da Windows Image Acquisition (WIA) 2,0.

## <a name="members"></a>Membri

L'interfaccia **IWiaImageFilter** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaImageFilter** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWiaImageFilter** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ApplyProperties**](-wia-iwiaimagefilter-applyproperties.md)       | Consente al filtro di elaborazione delle immagini di scrivere di nuovo le proprietà sul driver (e sul dispositivo).<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | Filtra l'immagine di anteprima.<br/>                                                                   |
| [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)     | Inizializza il filtro. Chiamato da WIA 2,0 prima del download di ogni immagine. <br/>                       |
| [**SetNewCallback**](-wia-iwiaimagefilter-setnewcallback.md)         | Imposta un nuovo callback dell'applicazione per il filtro di elaborazione dell'immagine da utilizzare per l'invio delle chiamate.<br/> |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori del filtro per l'elaborazione delle immagini devono implementare questa interfaccia e l'interfaccia [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) .

WIA 2,0 chiama i metodi di filtro. Non vengono mai chiamati direttamente da un'applicazione.

Microsoft fornisce il componente di anteprima WIA 2,0, che memorizza nella cache l'immagine di anteprima originale non filtrata acquisita dallo scanner. Un'applicazione utilizza [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare co-creazione di un'istanza del componente WIA 2,0 Preview (CLSID \_ WiaPreview), che carica il filtro utilizzando [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md). Il filtro viene chiamato automaticamente quando l'applicazione chiama [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md).

Il filtro di elaborazione delle immagini viene sempre eseguito quando viene eseguita l'analisi di un'immagine. Un'applicazione non può acquisire un'immagine dallo scanner senza che sia stato applicato per primo il filtro per la creazione di immagini.

Un filtro deve implementare una luminosità e un contrasto minimo. L'interfaccia utente comune, che fornisce controlli di luminosità e contrasto all'utente, può visualizzare anteprime accurate per l'utente.

Un filtro di elaborazione immagini non deve mai modificare il membro *lMessage* della struttura [**WiaTransferParams**](-wia-wiatransferparams.md) .

Per leggere le proprietà obbligatorie, il filtro di elaborazione delle immagini deve chiamare [**IWiaPropertyStorage:: GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) sull'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) ottenuta dall'elemento chiamando [IWiaImageFilter:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Il filtro può quindi creare un'istanza di [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) in questo flusso per leggere le proprietà degli elementi. Il filtro di elaborazione delle immagini non deve chiamare direttamente [IWiaPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) perché questo metodo effettua una chiamata all'oggetto del driver `drvReadItemProperties` , ma il servizio WIA 2,0 ha già bloccato il driver nella chiamata, in `drvAcquireItemData` modo che la chiamata venga interrotta e avrà esito negativo.

Le proprietà a cui è interessato il filtro possono ad esempio essere le impostazioni di luminosità e contrasto. Il filtro deve in genere anche leggere il formato dell'immagine, nonché la proprietà di anteprima, [**WIA \_ DPS \_ Preview**](-wia-wiaitempropscannerdevice.md), di *pWiaItem2*. Queste proprietà vengono tutte utilizzate nel processo di filtraggio.

I componenti WIA 2,0 scrivono sempre i dati non filtrati nel filtro di elaborazione delle immagini. L'algoritmo di elaborazione delle immagini implementato dal flusso del filtro può filtrare i dati più di una volta e non è necessario preoccuparsi di produrre gli stessi risultati che filtrano i dati una sola volta.

Il filtro deve prestare attenzione alla proprietà [**di \_ \_ Anteprima WIA DPS**](-wia-wiaitempropscannerdevice.md) , soprattutto se alcune attività correlate al filtro vengono gestite nell'hardware. Un determinato driver, ad esempio, può modificare la luminosità della lampada nell'hardware dello scanner, a seconda del modo in cui l'applicazione ha impostato la luminosità in un elemento WIA 2,0. Durante l'analisi finale (quando l'applicazione chiama [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md)), il driver in genere modifica la lampada fisica dello scanner. In questo caso il filtro di elaborazione delle immagini potrebbe non dover eseguire alcuna elaborazione della luminosità. Durante un'analisi di anteprima, tuttavia, il driver non deve modificare la luminosità della lampada, ma deve essere eseguita esclusivamente nel filtro di elaborazione delle immagini. È importante che il componente di anteprima WIA 2,0 e il filtro di elaborazione immagini restituiscano immagini accurate in base alle proprietà impostate nell'elemento.

Un filtro di elaborazione immagini deve supportare tutti i formati di immagine supportati dal driver.

Al filtro di elaborazione delle immagini viene sempre assegnata un'immagine corrispondente all'area di selezione impostata nell'elemento per il quale si sta acquisendo l'immagine. Si noti, tuttavia, che l'immagine potrebbe essere stata ruotata dal driver in caso di supporto della proprietà di [**\_ \_ rotazione degli indirizzi IP WIA**](-wia-wiaitempropscanneritem.md) .

Il filtro di elaborazione delle immagini viene creato tramite [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md), in genere non dall'applicazione, ma dai componenti WIA 2,0 quando un'applicazione chiama [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) o [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md).

L'interfaccia **IWiaImageFilter** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
