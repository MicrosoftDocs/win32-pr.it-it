---
description: Si applica a Windows Vista e versioni successive.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e376c6e95160c6a6c3c6637a765d868e282d33
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910239"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>Proprietà AM \_ RATE \_ ReverseMaxFullDataRate

Si applica a Windows Vista e versioni successive.

Restituisce la velocità massima di riproduzione inversa del decodificatore. Il valore della proprietà è il valore assoluto della velocità inversa massima x 10000. Ad esempio, se la velocità inversa massima è -2,0, il valore di questa proprietà è 20000.

Il tipo di dati per questa proprietà **è AM \_ MaxFullDataRate,** che è un `typedef` per **LONG.**

Questa proprietà è di sola lettura.



| Label | Valore |
|-------------------|----------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange    |
| ID proprietà       | AM \_ RATE \_ ReverseMaxFullDataRate |
| Tipo di dati         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>Commenti

I decodificatori che supportano la riproduzione inversa uniforme devono esporre questa proprietà. Per altre informazioni, vedere [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




