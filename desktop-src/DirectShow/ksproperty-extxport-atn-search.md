---
description: Questa proprietà Invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN). Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303711"
---
# <a name="ksproperty_extxport_atn_search"></a>\_ricerca KSPROPERTY EXTXPORT \_ ATN \_

Questa proprietà Invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN). Il driver di dispositivo UVC supporta questa proprietà.



|                   |                                       |
|-------------------|---------------------------------------|
| GUID set di proprietà | \_trasporto PROPSETID ext \_             |
| ID proprietà       | \_ricerca KSPROPERTY EXTXPORT \_ ATN \_     |
| Tipo di dati         | **KSPROPERTY \_ Struttura EXTXPORT \_ S** |



 

## <a name="remarks"></a>Commenti

Impostare il membro **dwAbsTrackNumber** della struttura **KSPROPERTY \_ EXTXPORT \_ S** sul valore seguente:


```
(absolute track number << 1) + continuity bit
```



La specifica UVC non definisce il modo in cui il dispositivo usa il bit di continuità. La struttura **KSPROPERTY \_ EXTXPORT \_ S** è descritta nel DDK di Windows.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà di trasporto dispositivo esterno](external-device-transport-property-set.md)
</dt> </dl>

 

 



