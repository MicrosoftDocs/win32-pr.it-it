---
description: Il metodo SelectAndActivateButton seleziona e attiva il pulsante specificato.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Metodo SelectAndActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d141616356db5daf2ebcb19579b924f6d4cab956e03d876d0254666d55b5702b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951910"
---
# <a name="selectandactivatebutton-method"></a>Metodo SelectAndActivateButton

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SelectAndActivateButton` metodo seleziona e attiva il pulsante specificato.

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*Ibutton*
</dt> <dd>

Specifica il pulsante come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Usare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione [**di DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true.**

Questo metodo evidenzia il pulsante specificato e lo attiva automaticamente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PulsantiDisponibili**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



