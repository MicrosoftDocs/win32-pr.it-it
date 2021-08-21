---
title: Scomparti
description: Scomparti
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Framework servizi di testo (TSF), raggruppamenti
- TSF (Framework servizi di testo), raggruppamenti
- servizi di testo, raggruppamenti
- Applicazioni abilitate per TSF, raggruppamenti
- Scomparti
- Framework servizi di testo (TSF), tipi di raggruppamento
- TSF (Framework servizi di testo), tipi di raggruppamento
- servizi di testo, tipi di raggruppamento
- Applicazioni abilitate per TSF, tipi di raggruppamento
- tipi di raggruppamento
- Framework servizi di testo (TSF), notifiche di modifica raggruppamento
- TSF (Framework servizi di testo), notifiche di modifica raggruppamento
- servizi di testo, notifiche di modifica raggruppamento
- Applicazioni abilitate per TSF, notifiche di modifica raggruppamento
- notifiche di modifica raggruppamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ff74cf3c98f99aa2462da8c0bfe1505b555b879f4d4e38f51e57ccc239a78f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879838"
---
# <a name="compartments"></a>Scomparti

## <a name="compartment-types"></a>Tipi di raggruppamento

Esistono diversi tipi di raggruppamenti. Esiste un raggruppamento globale e ogni gestore di thread, gestore di documenti e contesto può contenere un raggruppamento.

Il raggruppamento globale consente ai client di condividere i dati tra processi. Per ottenere il gestore raggruppamento globale, chiamare [**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).

Il gestore di thread contiene un gestore raggruppamenti che contiene raggruppamenti per ogni thread. In questo modo i dati possono essere condivisi all'interno di un thread. Per ottenere un gestore raggruppamenti di thread manager, chiamare **ITfThreadMgr::QueryInterface** con IID \_ ITfCompartmentMgr.

Ogni gestore di documenti creato contiene anche un gestore raggruppamenti. In questo modo i dati possono essere condivisi all'interno di un gestore di documenti specifico. Per ottenere il gestore raggruppamenti di gestione documenti, chiamare **ITfDocumentMgr::QueryInterface** con IID \_ ITfCompartmentMgr.

Ogni contesto creato contiene anche un gestore raggruppamenti. In questo modo i dati possono essere condivisi all'interno di un contesto specifico. Per ottenere un gestore raggruppamento di contesto, chiamare **ITfContext::QueryInterface** con IID \_ ITfCompartmentMgr.

## <a name="creating-and-deleting-a-compartment"></a>Creazione ed eliminazione di un raggruppamento

Viene creato un raggruppamento la prima volta che viene chiamato [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) con il GUID del raggruppamento. Il client di installazione deve impostare il valore iniziale del raggruppamento [**usando ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue). Finché non viene impostato un valore, il valore del raggruppamento è vuoto. Per questo scopo, non è possibile verificare che il raggruppamento esistesse prima della **chiamata a GetCompartment.** Per evitare questa situazione, il client di installazione deve impostare il valore su un valore iniziale in modo che altri client possano determinare se il raggruppamento esiste già.

Il [**metodo ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) viene usato per rimuovere un raggruppamento. Tutti i riferimenti esistenti al raggruppamento sono contrassegnati come non validi.

## <a name="obtaining-compartments"></a>Recupero di raggruppamenti

Usando [**l'interfaccia ITfCompartmentMgr,**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) un client può enumerare i raggruppamenti chiamando [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments). Questo metodo fornisce un **oggetto IEnumGUID** che contiene i GUID di tutti i raggruppamenti installati.

Usando il GUID del raggruppamento, **ITfCompartmentMgr::GetCompartment** viene usato per ottenere un raggruppamento specifico. Questo metodo fornisce al chiamante un [**oggetto ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) che può ottenere e impostare i dati del raggruppamento.

## <a name="receiving-compartment-change-notifications"></a>Ricezione di notifiche di modifica raggruppamento

Quando il valore di un raggruppamento cambia, il gestore TSF notifica ai sink di notifica installati che il raggruppamento è stato modificato. Per installare un sink di notifica delle modifiche di raggruppamento, creare un oggetto che implementa [**ITfCompartmentEventSink.**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink) Chiamare quindi **ITfCompartment::QueryInterface** con IID ITfSource sull'oggetto raggruppamento da monitorare per \_ ottenere [**un'interfaccia ITfSource.**](/windows/desktop/api/Msctf/nn-msctf-itfsource) Chiamare ora [**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfCompartmentEventSink e il puntatore **all'oggetto ITfCompartmentEventSink.** Quando il valore del raggruppamento cambia, il metodo [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) del sink di consulenza viene chiamato con il GUID del raggruppamento. Il sink di consulenza può chiamare [**ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) per ottenere il nuovo valore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[**TfClientId**](tfclientid.md)
</dt> <dt>

[**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




