---
description: Questa proprietà invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN). Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d35c1fce1e958aa475cc0344c2db320daa806326a49d0d6e939bf4ea86d49f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823271"
---
# <a name="ksproperty_extxport_atn_search"></a>KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH

Questa proprietà invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN). Il driver di dispositivo UVC supporta questa proprietà.



| Etichetta | Valore |
|-------------------|---------------------------------------|
| GUID set di proprietà | PROPSETID \_ EXT \_ TRANSPORT             |
| ID proprietà       | KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH     |
| Tipo di dati         | **KSPROPERTY \_ Struttura EXTXPORT \_ S** |



 

## <a name="remarks"></a>Commenti

Impostare il **membro dwAbsTrackNumber** della **struttura KSPROPERTY \_ EXTXPORT \_ S** sul valore seguente:


```
(absolute track number << 1) + continuity bit
```



La specifica UVC non definisce il modo in cui il dispositivo usa il bit di continuità. La **struttura KSPROPERTY \_ EXTXPORT \_ S** è descritta nel Windows DDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà trasporto dispositivo esterno](external-device-transport-property-set.md)
</dt> </dl>

 

 



