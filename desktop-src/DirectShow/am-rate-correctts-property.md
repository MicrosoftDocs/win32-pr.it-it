---
description: Lo strumento di navigazione DVD usa questa proprietà per informare il decodificatore che lo strumento di navigazione sta impostando i timestamp corretti nei campioni recapitati al decodificatore.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858195ee6366be385a0d192a73b4375d43cae58cb574da2795efc87f78651ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052921"
---
# <a name="am_rate_correctts-property"></a>Proprietà AM \_ RATE \_ CorrectTS

Lo strumento di navigazione DVD usa questa proprietà per informare il decodificatore che lo strumento di navigazione sta impostando i timestamp corretti nei campioni recapitati al decodificatore.



| Etichetta | Valore |
|-------------------|-------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange |
| ID proprietà       | AM \_ RATE \_ CorrectTS           |
| Tipo di dati         | **LONG**                      |



 

## <a name="remarks"></a>Commenti

Le versioni precedenti di DVD Navigator non impostano i timestamp corretti quando la velocità di riproduzione è diversa da 1.0. Molti decodificatori rilascino questo problema ignorando i timestamp durante il riavvolgimento o l'avanzamento rapido e stimando i tempi di presentazione corretti.

Questi problemi sono stati corretti nella versione corrente dello strumento di navigazione DVD. Per garantire la compatibilità con le versioni precedenti con i decodificatori esistenti, lo strumento di navigazione DVD indica che i timestamp sono corretti impostando la proprietà AM RATE CorrectTS sul \_ \_ decodificatore con il valore **TRUE**. Quando questa proprietà è impostata, il decodificatore deve usare i timestamp effettivi, anziché stimare gli orari di presentazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostare le proprietà di modifica della frequenza**](rate-change-property-set.md)
</dt> </dl>

 

 




