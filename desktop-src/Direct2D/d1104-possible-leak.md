---
title: D1104 Possibile perdita
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: La factory è stata rilasciata ma l'interfaccia creata da essa è ancora attiva. Anche se è valido rilasciare le risorse dopo il rilascio della factory, questa condizione potrebbe essere indicativa di una perdita di memoria.
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
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548676"
---
# <a name="d1104-possible-leak"></a>D1104: possibile perdita

La factory \[ *factory è* \] stata rilasciata, ma l'interfaccia creata da essa è ancora \[  \] attiva. Anche se è valido rilasciare le risorse dopo il rilascio della factory, questa condizione potrebbe essere indicativa di una perdita di memoria.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*Fabbrica*
</dt> <dd>

Indirizzo della factory rilasciata.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia creata nella *factory*.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Livello di errore | Informazioni |



 

## <a name="possible-causes"></a>Possibili cause

La factory è stata rilasciata ma l'interfaccia creata da essa è ancora attiva.

 

 




