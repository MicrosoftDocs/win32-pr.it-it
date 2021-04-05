---
title: D1104 possibile perdita
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: La Factory è stata rilasciata, ma l'interfaccia creata è ancora attiva. Sebbene sia possibile rilasciare le risorse dopo aver rilasciato la Factory, questa condizione potrebbe essere indicativa di una perdita di memoria.
keywords:
- D1104 possibile perdita di Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333556"
---
# <a name="d1104-possible-leak"></a>D1104: possibile perdita

Factory factory \[ *è* \] stata rilasciata, ma l' \[ *interfaccia* \] di interfaccia creata da essa è ancora attiva. Sebbene sia possibile rilasciare le risorse dopo aver rilasciato la Factory, questa condizione potrebbe essere indicativa di una perdita di memoria.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*fabbrica*
</dt> <dd>

Indirizzo della Factory rilasciata.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia creata nella *Factory*.

</dd> </dl> 

|             |             |
|-------------|-------------|
| Livello di errore | Informazioni |



 

## <a name="possible-causes"></a>Possibili cause

La Factory è stata rilasciata, ma l'interfaccia creata è ancora attiva.

 

 




