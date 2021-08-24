---
description: Il metodo DVDAdm.GetParentalCountry recupera il paese/area geografica dei genitori salvato per ultimo nel registro.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Metodo GetParentalCountry (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeeee55a3e39449c48e1af6b2674db85d5c4a964e730e5a66bb91be6dca2c393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756761"
---
# <a name="getparentalcountry-method"></a>Metodo GetParentalCountry

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.GetParentalCountry` metodo recupera l'ultimo paese/area geografica dei genitori salvato nel registro.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Valore restituito

Restituisce un intero che indica il codice paese/area geografica predefinito archiviato nel Registro di sistema.

## <a name="remarks"></a>Commenti

Il paese/area geografica dei genitori recuperato da questo metodo non corrisponde necessariamente allo stesso paese/area geografica attualmente archiviato nell'oggetto MSWebDVD.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




