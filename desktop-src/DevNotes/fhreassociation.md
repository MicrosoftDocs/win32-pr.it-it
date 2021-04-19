---
description: Rappresenta la funzionalità di riassociazione cronologia file che consente a un utente di ristabilire una relazione con una destinazione di backup utilizzata dallo stesso utente in passato. La riassociazione viene eseguita chiamando i metodi dell'interfaccia IFhReassociation.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Classe FhReassociation (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304844"
---
# <a name="fhreassociation-class"></a>Classe FhReassociation

Rappresenta la funzionalità di riassociazione cronologia file che consente a un utente di ristabilire una relazione con una destinazione di backup utilizzata dallo stesso utente in passato. La riassociazione viene eseguita chiamando i metodi dell'interfaccia [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .

## <a name="when-to-implement"></a>Quando implementare

L'API cronologia file implementa questa classe. Per creare un'istanza di questa classe, utilizzare la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Fhcfg. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Fhcfg. idl</dt> </dl> |



 

 
