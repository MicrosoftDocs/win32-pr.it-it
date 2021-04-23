---
description: Questa proprietà invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN). Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909448"
---
# <a name="ksproperty_extxport_atn_search"></a>KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH

Questa proprietà invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN). Il driver di dispositivo UVC supporta questa proprietà.



| Label | Valore |
|-------------------|---------------------------------------|
| GUID set di proprietà | PROPSETID \_ EXT \_ TRANSPORT             |
| ID proprietà       | KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH     |
| Tipo di dati         | **KSPROPERTY \_ Struttura EXTXPORT \_ S** |



 

## <a name="remarks"></a>Commenti

Impostare il **membro dwAbsTrackNumber** della **struttura KSPROPERTY \_ EXTXPORT \_ S** sul valore seguente:


```
(absolute track number << 1) + continuity bit
```



La specifica UVC non definisce il modo in cui il dispositivo usa il bit di continuità. La **struttura KSPROPERTY \_ EXTXPORT \_ S** è descritta in Windows DDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà Trasporto dispositivo esterno](external-device-transport-property-set.md)
</dt> </dl>

 

 



