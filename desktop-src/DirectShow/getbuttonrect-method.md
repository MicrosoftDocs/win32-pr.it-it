---
description: Il metodo GetButtonRect Recupera il rettangolo per il pulsante specificato, nelle coordinate della finestra.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Metodo GetButtonRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123534"
---
# <a name="getbuttonrect-method"></a>Metodo GetButtonRect

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetButtonRect` metodo recupera il rettangolo per il pulsante specificato, in coordinate della finestra.

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*
</dt> <dd>

Specifica il numero di pulsante come intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un oggetto [DVDRect](dvdrect-object.md) che definisce il rettangolo.

## <a name="remarks"></a>Commenti

Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



