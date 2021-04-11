---
description: Il metodo GetButtonAtPosition Recupera il numero del pulsante in corrispondenza delle coordinate specificate senza selezionarlo o attivarlo.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Metodo GetButtonAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123537"
---
# <a name="getbuttonatposition-method"></a>Metodo GetButtonAtPosition

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetButtonAtPosition` metodo recupera il numero del pulsante in corrispondenza delle coordinate specificate senza selezionarlo o attivarlo.

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Specifica la coordinata x del puntatore del mouse come intero.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Specifica la coordinata y del puntatore del mouse come intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che specifica il pulsante, se presente, in corrispondenza della posizione specificata.

## <a name="remarks"></a>Commenti

Questo metodo restituisce zero se non è presente alcun pulsante in corrispondenza delle coordinate specificate. Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



