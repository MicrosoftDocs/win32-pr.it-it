---
title: CGENOBJ. CPP
description: Nella tabella seguente sono elencati i metodi generici dell'oggetto Active Directory supportati in cgenobj.cpp nel componente provider di esempio.
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0667d44bfb3861989a58ac3764a113b4eb23a87ce3722709a5ca959a0fe4da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962100"
---
# <a name="cgenobjcpp"></a>CGENOBJ. CPP

Nella tabella seguente sono elencati i metodi generici dell'oggetto Active Directory supportati in cgenobj.cpp nel componente provider di esempio.



| Metodo                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObject::CSampleDSGenObject**                                              | Costruttore standard.                                                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::~CSampleDSGenObject**                                             | Distruttore standard.                                                                                                                                                                                                                                                                                                        |
| **CSampleDSGenObject::CreateGenericObject**                                             | Creare un oggetto generico ADS. Inizializzare in base alle esigenze.                                                                                                                                                                                                                                                                    |
| **CSampleDSGenObject::SampleDSCreateObject**                                            | Creare questo oggetto nel contenitore padre.                                                                                                                                                                                                                                                                                 |
| **CSampleDSGenObject::SampleDSSetObject**                                               | Salvare le proprietà di questo oggetto (cancellare la cache).                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::AllocateGenObject**                                               | Creare un oggetto generico e caricarne i dati di tipo.                                                                                                                                                                                                                                                                             |
| **CSampleDSGenObject::QueryInterface**                                                  | Restituisce il puntatore a interfaccia richiesto, se disponibile.                                                                                                                                                                                                                                                                       |
| Metodi [**IAD**](/windows/desktop/api/Iads/nn-iads-iads) standard, incluse le implementazioni per:                   | [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) (incluso il mapping dal tipo di dati nativo al tipo VARIANT) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) (incluso il mapping dal tipo VARIANT al tipo di dati nativo)<br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (aggiornare la cache delle proprietà)<br/> [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) (salva la cache delle proprietà)<br/> |
| Metodi [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) standard, incluse le implementazioni per: | [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**Get \_ Filter**](iadscontainer-property-methods.md)<br/> [**Crea**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**Elimina**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **ConvertSafeArrayToVariantArray**                                                      | Routine di utilità.                                                                                                                                                                                                                                                                                                            |



 

 

 





