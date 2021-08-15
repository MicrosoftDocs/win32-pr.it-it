---
title: Recupero delle proprietà di accounting
description: L'oggetto accounting è uno degli oggetti nella raccolta Request Handlers.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77390a6aa67e946de6d69dd3d1bc28a76907b7ad31b497d4921c7a2d7493c328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361729"
---
# <a name="obtaining-accounting-properties"></a>Recupero delle proprietà di accounting

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'oggetto accounting è uno degli oggetti nella raccolta Request Handlers. Il valore di enumerazione per la raccolta di gestori richieste è **PROPERTY \_ IAS \_ REQUESTHANDLERS \_ COLLECTION**. Il nome del gestore per l'oggetto accounting è "Microsoft Accounting".

Nell'esempio Visual Basic codice accede alle proprietà disponibili dal gestore dell'oggetto accounting.


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



Per accedere alle proprietà di accounting usando C++, ottenere prima di tutto la raccolta di gestori di richieste. [L'oggetto Recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection) contiene codice C++ che illustra come ottenere una raccolta. Il valore di enumerazione per la raccolta di gestori richieste è **PROPERTY \_ IAS \_ REQUESTHANDLERS \_ COLLECTION**. I valori corrispondenti alle varie raccolte di Server dei criteri di rete vengono enumerati dal [**tipo di enumerazione IASPROPERTIES.**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)

La raccolta dei gestori richieste contiene un oggetto denominato "Microsoft Accounting". Recuperare questo oggetto dalla raccolta. La sezione [Recupero di un oggetto da](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) una raccolta contiene codice C++ che illustra come ottenere un oggetto da una raccolta.

Dopo aver creato l'oggetto Microsoft Accounting, ottenere [**un'interfaccia ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) per l'oggetto [**usando IUnknown::QueryInterface.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) La sezione [Recupero di un SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) utente contiene codice C++ che illustra come ottenere **un'interfaccia ISdo** per un oggetto. È quindi possibile usare il [**metodo ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) per ottenere i valori delle proprietà per l'oggetto Microsoft Accounting.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Recupero di un oggetto da una raccolta](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Recupero di un SDO utente](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**PROPRIETÀ IAS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 