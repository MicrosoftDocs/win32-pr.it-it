---
description: Questa proprietà esegue una query sul decodificatore per l'ora di inizio della modifica della frequenza accodata più di recente, indipendentemente dalla posizione nella coda di modifica della frequenza.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e7b54e618829d9768b4d08a0a76defcf2c91758be6b916b6e570b368191e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824835"
---
# <a name="am_rate_querylastratesegpts-property"></a>Am \_ RATE \_ QueryLastRateSegPTS - proprietà

Questa proprietà esegue una query sul decodificatore per l'ora di inizio della modifica della frequenza accodata più di recente, indipendentemente dalla posizione nella coda di modifica della frequenza.

Questa proprietà è definita per la versione 1.1 di questo set di proprietà. vedere [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Etichetta | Valore |
|-------------------|-------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange |
| ID proprietà       | AM \_ RATE \_ QueryLastRateSegPTS |
| Tipo di dati         | **TEMPO DI \_ RIFERIMENTO**           |



 

## <a name="remarks"></a>Commenti

Il filtro di origine può usare questa proprietà per sincronizzare le modifiche della frequenza tra diversi flussi audio e video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostare la proprietà Rate Change**](rate-change-property-set.md)
</dt> </dl>

 

 




