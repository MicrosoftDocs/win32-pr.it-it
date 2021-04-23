---
description: Lo strumento di navigazione DVD usa questa proprietà per informare il decodificatore che lo Strumento di navigazione sta impostando i timestamp corretti nei campioni che recapita al decodificatore.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910299"
---
# <a name="am_rate_correctts-property"></a>Am \_ RATE \_ CorrectTS - proprietà

Lo strumento di navigazione DVD usa questa proprietà per informare il decodificatore che lo Strumento di navigazione sta impostando i timestamp corretti nei campioni che recapita al decodificatore.



| Label | Valore |
|-------------------|-------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange |
| ID proprietà       | AM \_ RATE \_ CorrectTS           |
| Tipo di dati         | **LONG**                      |



 

## <a name="remarks"></a>Commenti

Le versioni precedenti dello strumento di spostamento DVD non impostano i timestamp corretti quando la velocità di riproduzione è diversa da 1.0. Molti decodificatori rilascino questo problema ignorando i timestamp durante il riavvolgimento o l'avanzamento rapido e stimando i tempi di presentazione corretti.

Questi problemi sono stati corretti nella versione corrente dello Strumento di navigazione DVD. Per garantire la compatibilità con le versioni precedenti dei decodificatori esistenti, lo strumento di spostamento DVD indica che i timestamp sono corretti impostando la proprietà AM RATE CorrectTS sul decodificatore con il \_ \_ valore **TRUE**. Quando questa proprietà è impostata, il decodificatore deve usare i timestamp effettivi anziché stimare l'ora di presentazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




