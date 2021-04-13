---
description: Fornisce l'accesso alle proprietà dell'oggetto di contesto correlate alle transazioni.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Interfaccia IContextTransactionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483437"
---
# <a name="icontexttransactioninfo-interface"></a>Interfaccia IContextTransactionInfo

Fornisce l'accesso alle proprietà dell'oggetto di contesto correlate alle transazioni.

## <a name="when-to-implement"></a>Quando implementare

Non implementare questa interfaccia. L'implementazione standard offre funzionalità complete.

## <a name="when-to-use"></a>Utilizzo

Utilizzare questa interfaccia per accedere alle proprietà dell'oggetto di contesto correlate alle transazioni.

## <a name="members"></a>Membri

L'interfaccia **IContextTransactionInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextTransactionInfo** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IContextTransactionInfo** dispone di questi metodi.



| Metodo                                                                                         | Descrizione                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**FetchTransaction**](icontexttransactioninfo-registertransactionproxy.md)                   | Recupera la transazione o il proxy di transazione associato al contesto corrente, se presente.<br/>              |
| [**GetTxIsolationLevelAndTimeout**](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | Recupera il livello di isolamento e il valore di timeout di una transazione ospitata nel contesto di transazione radice.<br/> |
| [**RegisterTransactionProxy**](icontexttransactioninfo-fetchtransaction.md)                   | Associa un'implementazione di [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) al contesto corrente.<br/>            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>          |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/> |



 

