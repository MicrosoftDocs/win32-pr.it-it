---
title: Violazione del threading D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: È stato eseguito l'accesso simultaneo a un'interfaccia con thread a noleggio da più thread.
keywords:
- D1105 Violazione del threading Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 12e7321fd40437bc262439c6ddb319a0aa6dba145d05d3feebba2813c904bbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537971"
---
# <a name="d1105-threading-violation"></a>D1105: Violazione del threading

È stato eseguito l'accesso \[ *simultaneo a* \] un'interfaccia a thread di noleggio da più thread.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia a cui hanno avuto accesso più thread.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possibili cause

Uso di un'istanza dell'oggetto dalla stessa factory a thread singolo da due thread diversi.

 

 




