---
description: Questa proprietà esegue una query sul decodificatore per ottenere la frequenza massima dei frame completa supportata dal decodificatore. Il tipo di dati di questa proprietà è una \_ struttura am QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Proprietà AM_RATE_QueryFullFrameRate (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330331"
---
# <a name="am_rate_queryfullframerate-property"></a>\_Proprietà rate \_ QueryFullFrameRate

Questa proprietà esegue una query sul decodificatore per ottenere la frequenza massima dei frame completa supportata dal decodificatore. Il tipo di dati di questa proprietà è una struttura **am \_ QueryRate** .

Questa proprietà è definita per la versione 1,1 di questo set di proprietà. vedere [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md).



|                   |                                       |
|-------------------|---------------------------------------|
| GUID set di proprietà | \_TSRateChange KSPROPSETID \_         |
| ID proprietà       | \_Proprietà rate \_ QueryFullFrameRate |
| Tipo di dati         | [**AM \_ QueryRate**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Commenti

Se la velocità di riproduzione supera la frequenza massima del decodificatore, il filtro di origine invia gruppi di campioni continui separati da discontinuità. Il timestamp passa attraverso le discontinuità. Il filtro di origine può eseguire questa operazione anche se la velocità di riproduzione rientra nella frequenza massima del decodificatore, perché potrebbero esserci altri fattori, ad esempio l'i/o del disco, che limitano la velocità di riproduzione completa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Set di proprietà di modifica della frequenza**](rate-change-property-set.md)
</dt> </dl>

 

 




