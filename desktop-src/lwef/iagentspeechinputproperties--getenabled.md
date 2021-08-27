---
title: IAgentSpeechInputProperties GetEnabled
description: IAgentSpeechInputProperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404bd6f0348487c8e039c247f5a9368359133be9e3df76b884115679a2961a97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114671"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a>IAgentSpeechInputProperties::GetEnabled

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

Recupera un valore che indica se il motore di riconoscimento vocale installato è abilitato.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Indirizzo di una variabile che riceve **True se** il motore di riconoscimento vocale è attualmente abilitato e **False se** disabilitato.

</dd> </dl>

 

 




