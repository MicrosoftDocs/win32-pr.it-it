---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750dbfee36039337025a03b9f77573a2134f85d15a56d77b2d512482c7bb0e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751455"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>IAgentAudioOutputProperties::GetUsingSoundEffects

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

Recupera un valore che indica se l'output degli effetti sonori è abilitato.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*
</dt> <dd>

Indirizzo di una variabile che riceve **True** se l'output degli effetti sonori è attualmente abilitato e **False** se disabilitato.

</dd> </dl>

Gli effetti sonori per l'animazione di un carattere vengono assegnati nell'editor di caratteri di Microsoft Agent. Poiché questa impostazione influisce sull'output degli effetti sonori per tutti i caratteri, solo l'utente può modificare questa proprietà nella finestra delle proprietà di Microsoft Agent.

 

 




