---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d144374f690d295b80d0092add56439eb4e5fc9d546ba1f970ab99976cf2d7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888392"
---
# <a name="iagentballoongetenabled"></a>IAgentBalloon::GetEnabled

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Recupera il valore della proprietà Enabled per [**un**](enabled-property.md) fumetto di parole.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Indirizzo di una variabile che riceve **True** quando il fumetto è abilitato e **False** quando è disabilitato.

</dd> </dl>

Il server Microsoft Agent visualizza automaticamente il fumetto per l'output vocale, a meno che non sia disabilitato. Il fumetto delle parole può essere disabilitato per un carattere nell'Editor caratteri di Microsoft Agent o (dall'utente) per tutti i caratteri nella finestra delle proprietà di Microsoft Agent. Se l'utente disabilita il fumetto, il client non può ripristinarlo.

 

 




