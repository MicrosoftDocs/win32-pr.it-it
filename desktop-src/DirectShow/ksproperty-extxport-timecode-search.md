---
description: Questa proprietà invia un comando al dispositivo per cercare un time code. Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909439"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH

Questa proprietà invia un comando al dispositivo per cercare un time code. Il driver di dispositivo UVC supporta questa proprietà.



| Label | Valore |
|-------------------|----------------------------------------|
| GUID set di proprietà | PROPSETID \_ EXT \_ TRANSPORT              |
| ID proprietà       | KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH |
| Tipo di dati         | **KSPROPERTY \_ Struttura EXTXPORT \_ S**  |



 

## <a name="remarks"></a>Commenti

Compilare il **membro Timecode** della struttura **KSPROPERTY \_ EXTXPORT \_ S** con il frame, il secondo, il minuto e l'ora desiderati. La **struttura KSPROPERTY \_ EXTXPORT \_ S** è descritta in Windows DDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà Trasporto dispositivo esterno](external-device-transport-property-set.md)
</dt> </dl>

 

 



