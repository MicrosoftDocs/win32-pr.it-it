---
description: Questa proprietà invia un comando al dispositivo per cercare un time code. Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f49b8e71d664cf266428d33c99b87859765623ca8205843bbfee108da5f7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153189"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH

Questa proprietà invia un comando al dispositivo per cercare un time code. Il driver di dispositivo UVC supporta questa proprietà.



| Etichetta | Valore |
|-------------------|----------------------------------------|
| GUID set di proprietà | PROPSETID \_ EXT \_ TRANSPORT              |
| ID proprietà       | KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH |
| Tipo di dati         | **KSPROPERTY \_ Struttura EXTXPORT \_ S**  |



 

## <a name="remarks"></a>Commenti

Compilare il **membro Timecode** della struttura **KSPROPERTY \_ EXTXPORT \_ S** con il frame, il secondo, il minuto e l'ora desiderati. La **struttura KSPROPERTY \_ EXTXPORT \_ S** è descritta nella Windows DDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà Trasporto dispositivo esterno](external-device-transport-property-set.md)
</dt> </dl>

 

 



