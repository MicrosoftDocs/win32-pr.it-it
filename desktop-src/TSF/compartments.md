---
title: Raggruppamenti
description: Raggruppamenti
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Framework servizi di testo (TSF), raggruppamenti
- TSF (Text Services Framework), raggruppamenti
- Servizi di testo, raggruppamenti
- Applicazioni abilitate per TSF, raggruppamenti
- raggruppamenti
- Framework servizi di testo (TSF), tipi di raggruppamento
- TSF (Framework dei servizi di testo), tipi di raggruppamento
- Servizi di testo, tipi di raggruppamento
- Applicazioni abilitate per TSF, tipi di raggruppamento
- tipi di raggruppamento
- Framework servizi di testo (TSF), notifiche di modifica raggruppamento
- TSF (Text Services Framework), notifiche di modifica di raggruppamento
- Servizi di testo, notifiche di modifica raggruppamento
- Applicazioni abilitate per TSF, notifiche di modifica del raggruppamento
- notifiche di modifica raggruppamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221185"
---
# <a name="compartments"></a>Raggruppamenti

## <a name="compartment-types"></a>Tipi di raggruppamento

Sono disponibili diversi tipi di raggruppamenti. È presente un raggruppamento globale e ogni gestore di thread, gestione documenti e contesto può contenere un raggruppamento.

Il raggruppamento globale consente ai client di condividere i dati tra i processi. Per ottenere il gestore di raggruppamento globale, chiamare [**ITfThreadMgr:: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).

Gestione thread contiene un gestore di raggruppamento che contiene i raggruppamenti in base ai singoli thread. In questo modo è possibile condividere i dati all'interno di un thread. Per ottenere un gestore di raggruppamento di gestione thread, chiamare **ITfThreadMgr:: QueryInterface** con IID \_ ITfCompartmentMgr.

Ogni gestore di documenti creato contiene anche un gestore di raggruppamento. In questo modo è possibile condividere i dati all'interno di un gestore di documenti specifico. Per ottenere il gestore di raggruppamento di gestione documenti, chiamare **ITfDocumentMgr:: QueryInterface** con IID \_ ITfCompartmentMgr.

Ogni contesto creato contiene anche un gestore di raggruppamento. In questo modo è possibile condividere i dati in un contesto specifico. Per ottenere un gestore di raggruppamento del contesto, chiamare **ITfContext:: QueryInterface** con IID \_ ITfCompartmentMgr.

## <a name="creating-and-deleting-a-compartment"></a>Creazione ed eliminazione di un raggruppamento

Viene creato un raggruppamento la prima volta che [**ITfCompartmentMgr:: Compartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) viene chiamato con il GUID di raggruppamento. Il client di installazione deve impostare il valore iniziale del raggruppamento usando [**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue). Fino a quando non viene impostato un valore, il valore del raggruppamento è vuoto. Per questo motivo, non esiste alcun modo per verificare che il raggruppamento esista prima della chiamata a **Compartment** . Per evitare questa situazione, il client di installazione deve impostare il valore su un valore iniziale, in modo che gli altri client possano determinare se il raggruppamento esiste già.

Il metodo [**ITfCompartmentMgr:: ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) viene usato per rimuovere un raggruppamento. Eventuali riferimenti esistenti al raggruppamento sono contrassegnati come non validi.

## <a name="obtaining-compartments"></a>Recupero di raggruppamenti

Usando l'interfaccia [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) , un client può enumerare i raggruppamenti chiamando [**ITfCompartmentMgr:: EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments). Questo metodo fornisce un oggetto **IEnumGUID** che contiene i GUID di tutti i raggruppamenti installati.

Usando il GUID di raggruppamento, **ITfCompartmentMgr:: Compartment** viene usato per ottenere un raggruppamento specifico. Questo metodo fornisce al chiamante un oggetto [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) che può ottenere e impostare i dati del raggruppamento.

## <a name="receiving-compartment-change-notifications"></a>Ricezione delle notifiche di modifica del raggruppamento

Quando viene modificato il valore di un raggruppamento, il gestore di TSF invia una notifica ai sink di avviso installati che il raggruppamento è stato modificato. Per installare un sink di notifica della modifica del raggruppamento, creare un oggetto che implementi [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink). Quindi, chiamare **ITfCompartment:: QueryInterface** con IID \_ ITfSource sull'oggetto Compartment da monitorare per ottenere un'interfaccia [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) . A questo punto, chiamare [**ITfSource:: adviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfCompartmentEventSink e il puntatore all'oggetto **ITfCompartmentEventSink** . Quando viene modificato il valore del raggruppamento, il sink di notifica [**ITfCompartmentEventSink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) viene chiamato con il GUID del raggruppamento. Il sink di notifica può chiamare [**ITfCompartment:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) per ottenere il nuovo valore.

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

[**ITfThreadMgr:: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[**ITfCompartmentMgr:: Compartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**ITfSource:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**ITfCompartmentEventSink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




