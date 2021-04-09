---
description: Questa proprietà Invia un comando al dispositivo per cercare un codice temporale specificato. Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048922"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ EXTXPORT \_ - \_ ricerca timecode

Questa proprietà Invia un comando al dispositivo per cercare un codice temporale specificato. Il driver di dispositivo UVC supporta questa proprietà.



|                   |                                        |
|-------------------|----------------------------------------|
| GUID set di proprietà | \_trasporto PROPSETID ext \_              |
| ID proprietà       | KSPROPERTY \_ EXTXPORT \_ - \_ ricerca timecode |
| Tipo di dati         | **KSPROPERTY \_ Struttura EXTXPORT \_ S**  |



 

## <a name="remarks"></a>Commenti

Compilare il membro **timecode** della struttura **KSPROPERTY \_ EXTXPORT \_** con il frame, il secondo, il minuto e l'ora desiderati. La struttura **KSPROPERTY \_ EXTXPORT \_ S** è descritta nel DDK di Windows.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà di trasporto dispositivo esterno](external-device-transport-property-set.md)
</dt> </dl>

 

 



