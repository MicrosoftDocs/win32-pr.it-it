---
description: Il navigatore DVD usa questa proprietà per informare il decodificatore che lo strumento di navigazione sta impostando i timestamp corretti sugli esempi che recapita al decodificatore.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Proprietà AM_RATE_CorrectTS (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330336"
---
# <a name="am_rate_correctts-property"></a>\_Proprietà rate \_ corrects

Il navigatore DVD usa questa proprietà per informare il decodificatore che lo strumento di navigazione sta impostando i timestamp corretti sugli esempi che recapita al decodificatore.



|                   |                               |
|-------------------|-------------------------------|
| GUID set di proprietà | \_TSRateChange KSPROPSETID \_ |
| ID proprietà       | \_Correttivi della velocità am \_           |
| Tipo di dati         | **LONG**                      |



 

## <a name="remarks"></a>Commenti

Le versioni precedenti di DVD Navigator non impostano i timestamp corretti quando la velocità di riproduzione è diversa da 1,0. Molti decodificatori aggirano questo problema ignorando gli indicatori temporali durante il rewind o l'avanzamento rapido e stimando i tempi di presentazione corretti.

Questi problemi sono stati corretti nella versione corrente del navigatore DVD. Per la compatibilità con le versioni precedenti dei decodificatori esistenti, il navigatore DVD indica che i timestamp sono corretti impostando la \_ Proprietà am rate \_ corrects nel decodificatore con il valore **true**. Quando questa proprietà è impostata, il decodificatore deve utilizzare i timestamp effettivi anziché stimare i tempi di presentazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Set di proprietà di modifica della frequenza**](rate-change-property-set.md)
</dt> </dl>

 

 




