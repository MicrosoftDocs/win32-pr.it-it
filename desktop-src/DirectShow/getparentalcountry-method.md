---
description: Il metodo DVDAdm. GetParentalCountry Recupera il paese padre/area che è stato salvato per ultimo nel registro di sistema.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Metodo GetParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330933"
---
# <a name="getparentalcountry-method"></a>Metodo GetParentalCountry

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.GetParentalCountry` metodo recupera il paese padre/area che è stato salvato per l'ultima volta nel registro di sistema.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Valore restituito

Restituisce un intero che indica il codice del paese/area geografica predefinito archiviato nel registro di sistema.

## <a name="remarks"></a>Commenti

Il paese/area padre recuperato da questo metodo non è necessariamente lo stesso paese/regione attualmente archiviato nell'oggetto MSWebDVD.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




