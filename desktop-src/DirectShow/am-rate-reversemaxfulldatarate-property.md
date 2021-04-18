---
description: Si applica a Windows Vista e versioni successive.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Proprietà AM_RATE_ReverseMaxFullDataRate (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330325"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>\_Proprietà rate \_ ReverseMaxFullDataRate

Si applica a Windows Vista e versioni successive.

Restituisce la frequenza massima di riproduzione inversa del decodificatore. Il valore della proprietà è il valore assoluto della velocità inversa massima x 10000. Se ad esempio la velocità massima inversa è-2,0, il valore di questa proprietà è 20000.

Il tipo di dati di questa proprietà **è \_ MaxFullDataRate**, che è un oggetto `typedef` per **Long**.

Questa proprietà è di sola lettura.



|                   |                                  |
|-------------------|----------------------------------|
| GUID set di proprietà | \_TSRateChange KSPROPSETID \_    |
| ID proprietà       | \_Frequenza \_ ReverseMaxFullDataRate |
| Tipo di dati         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>Commenti

I decodificatori che supportano la riproduzione Smooth inversa devono esporre questa proprietà. Per ulteriori informazioni, vedere [miglioramenti della riproduzione DVD in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Set di proprietà di modifica della frequenza**](rate-change-property-set.md)
</dt> </dl>

 

 




