---
description: Il metodo NotifyParentalLevelChange Abilita o Disabilita la gestione degli eventi per i comandi temporanei del livello di gestione padre.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Metodo NotifyParentalLevelChange (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328073"
---
# <a name="notifyparentallevelchange-method"></a>Metodo NotifyParentalLevelChange

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `NotifyParentalLevelChange` Metodo Abilita o Disabilita la gestione degli eventi per i comandi temporanei del livello di gestione padre.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*
</dt> <dd>

Specifica un valore booleano che indica se l'applicazione riceve una notifica quando l'oggetto MSWebDVD rileva segmenti video con una classificazione più restrittiva rispetto alla valutazione complessiva del disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le notifiche di gestione padre sono disabilitate per impostazione predefinita. Ciò significa che i comandi padre temporanei dal disco sono consentiti, ma ignorati e il disco verrà riprodotto senza interruzioni. Chiamare questo metodo durante l'inizializzazione dell'applicazione se è necessario gestire i comandi temporanei del livello di gestione padre dal disco. Per disabilitare la gestione padre dopo l'abilitazione, chiamare questo metodo con un argomento di false. Per ulteriori informazioni sulla gestione parentale, vedere [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 




