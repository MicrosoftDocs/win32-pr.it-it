---
description: La proprietà CurrentButton recupera il numero del pulsante di menu selezionato.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Proprietà CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b246b77283a2632f2feac4c2b374075ef9d9a205bcb71813856b9847df21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053141"
---
# <a name="currentbutton-property"></a>Proprietà CurrentButton

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentButton` proprietà recupera il numero del pulsante di menu selezionato.

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il pulsante.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito. Usare questo metodo quando si implementa la gestione personalizzata del mouse dopo [**l'impostazione di DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



