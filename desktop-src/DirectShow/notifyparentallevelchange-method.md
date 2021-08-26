---
description: Il metodo NotifyParentalLevelChange abilita o disabilita la gestione degli eventi per i comandi temporanei del livello di gestione genitori.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Metodo NotifyParentalLevelChange (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8382b52f64d4196b0ef74e5f3285e9bb047a4e1f77d3b0e5bec4da218ee753b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997361"
---
# <a name="notifyparentallevelchange-method"></a>Metodo NotifyParentalLevelChange

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo abilita o disabilita la gestione degli eventi per i comandi `NotifyParentalLevelChange` temporanei del livello di gestione dei genitori.

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*
</dt> <dd>

Specifica un valore booleano che indica se l'applicazione viene notificata quando l'oggetto MSWebDVD rileva segmenti video con una classificazione più restrittiva rispetto alla classificazione complessiva per il disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le notifiche di Gestione genitori sono disabilitate per impostazione predefinita. Ciò significa che i comandi temporanei dei genitori dal disco sono consentiti, ma ignorati e il disco verrà riprodotto senza interruzioni. Chiamare questo metodo durante l'inizializzazione dell'applicazione se è necessario gestire i comandi temporanei del livello di gestione dei genitori dal disco. Per disabilitare la gestione dei genitori dopo che è stata abilitata, chiamare questo metodo con un argomento false. Per altre informazioni sulla gestione dei genitori, vedere [**AcceptParentalLevelChange.**](acceptparentallevelchange-method.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segment.h</dt> </dl> |



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

[**SelezionareParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 




