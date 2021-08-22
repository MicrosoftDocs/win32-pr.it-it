---
description: La proprietà ButtonsAvailable recupera il numero totale di pulsanti nel menu corrente.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Proprietà ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16e14675238711ef0b572477334fecba0311ca2bb54d67fc3fe012ae6d1ede9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955560"
---
# <a name="buttonsavailable-property"></a>Proprietà ButtonsAvailable

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `ButtonsAvailable` proprietà recupera il numero totale di pulsanti nel menu corrente.

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il numero di pulsanti.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito. Usare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione [**di DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true.**

Chiamare questo metodo per recuperare il limite superiore per l'intervallo di numeri di pulsante validi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



