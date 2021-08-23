---
title: Possibile perdita D1104
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: La factory è stata rilasciata ma l'interfaccia creata da essa è ancora attiva. Anche se è possibile rilasciare le risorse dopo il rilascio della factory, questa condizione potrebbe essere indicativa di una perdita di memoria.
keywords:
- D1104 Possibile perdita Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b3c8b49256b3e7009985e9acf6d2b581e2fe436e50325c26f1f7de59cb3b0b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075565"
---
# <a name="d1104-possible-leak"></a>D1104: possibile perdita

La factory \[ *è stata* \] rilasciata ma l'interfaccia \[ *creata* da essa è \] ancora attiva. Anche se è possibile rilasciare le risorse dopo il rilascio della factory, questa condizione potrebbe essere indicativa di una perdita di memoria.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*Fabbrica*
</dt> <dd>

Indirizzo della factory rilasciata.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia creata nella *factory.*

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Livello di errore | Informazioni |



 

## <a name="possible-causes"></a>Possibili cause

La factory è stata rilasciata ma l'interfaccia creata da essa è ancora attiva.

 

 




