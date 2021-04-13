---
title: Recupero delle proprietà di contabilità
description: L'oggetto contabilità è uno degli oggetti nella raccolta di gestori di richieste.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399304"
---
# <a name="obtaining-accounting-properties"></a>Recupero delle proprietà di contabilità

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'oggetto contabilità è uno degli oggetti nella raccolta di gestori di richieste. Il valore di enumerazione per la raccolta di gestori di richieste è la **proprietà \_ IAS \_ REQUESTHANDLERS \_ Collection**. Il nome del gestore per l'oggetto contabilità è "contabilità Microsoft".

Il codice Visual Basic seguente accede alle proprietà disponibili dal gestore dell'oggetto contabilità.


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



Per accedere alle proprietà di contabilità con C++, ottenere prima la raccolta di gestori di richieste. Il [recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection) contiene codice C++ che illustra come ottenere una raccolta. Il valore di enumerazione per la raccolta di gestori di richieste è la **proprietà \_ IAS \_ REQUESTHANDLERS \_ Collection**. I valori corrispondenti alle varie raccolte NPS vengono enumerati dal tipo di enumerazione [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) .

La raccolta di gestori di richieste contiene un oggetto denominato "Microsoft Accounting". Recuperare questo oggetto dalla raccolta. La sezione [recupero di un oggetto da una raccolta](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contiene codice C++ che illustra come ottenere un oggetto da una raccolta.

Una volta ottenuto l'oggetto Accounting Microsoft, ottenere un'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) per l'oggetto usando [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). La sezione [recupero di un SDO utente](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contiene codice C++ che illustra come ottenere un'interfaccia **ISdo** per un oggetto. È quindi possibile usare il metodo [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) per ottenere i valori delle proprietà per l'oggetto Accounting Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Recupero di un oggetto da una raccolta](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Recupero di un utente SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 