---
title: CGENOBJ. CPP
description: Nel componente provider di esempio, i metodi dell'oggetto Active Directory generici, supportati in cgenobj. cpp, sono elencati nella tabella seguente.
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe769dcfa6e4ab607188728115bcba16e40c0e56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707468"
---
# <a name="cgenobjcpp"></a>CGENOBJ. CPP

Nel componente provider di esempio, i metodi dell'oggetto Active Directory generici, supportati in cgenobj. cpp, sono elencati nella tabella seguente.



| Metodo                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObject::CSampleDSGenObject**                                              | Costruttore standard.                                                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject:: ~ CSampleDSGenObject**                                             | Distruttore standard.                                                                                                                                                                                                                                                                                                        |
| **CSampleDSGenObject::CreateGenericObject**                                             | Creazione di un oggetto generico ADS. Inizializzare nel modo appropriato.                                                                                                                                                                                                                                                                    |
| **CSampleDSGenObject::SampleDSCreateObject**                                            | Creare questo oggetto nel contenitore padre.                                                                                                                                                                                                                                                                                 |
| **CSampleDSGenObject::SampleDSSetObject**                                               | Salva le proprietà di questo oggetto (Cancella la cache).                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::AllocateGenObject**                                               | Creare un oggetto generico e caricare i dati di tipo.                                                                                                                                                                                                                                                                             |
| **CSampleDSGenObject:: QueryInterface**                                                  | Restituisce il puntatore a interfaccia richiesto, se disponibile.                                                                                                                                                                                                                                                                       |
| Metodi [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard, incluse le implementazioni per:                   | [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) (incluso il mapping dal tipo di dati nativo al tipo Variant) [**put**](/windows/desktop/api/Iads/nf-iads-iads-put) (incluso il mapping dal tipo Variant al tipo di dati nativo)<br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (aggiornamento della cache delle proprietà)<br/> [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) (salvare la cache delle proprietà)<br/> |
| Metodi [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) standard, incluse le implementazioni per: | [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**Ottieni \_ filtro**](iadscontainer-property-methods.md)<br/> [**Creare**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **ConvertSafeArrayToVariantArray**                                                      | Routine di utilità.                                                                                                                                                                                                                                                                                                            |



 

 

 





