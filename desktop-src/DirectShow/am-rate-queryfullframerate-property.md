---
description: Questa proprietà esegue una query sul decodificatore per la frequenza massima di fotogrammi completi supportati dal decodificatore. Il tipo di dati per questa proprietà è una struttura \_ AM QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ceb938ac3fd0ea5f7f58b340f4b57fd6a722650cd3225702cbb74b1644045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664109"
---
# <a name="am_rate_queryfullframerate-property"></a>Am \_ RATE \_ QueryFullFrameRate - proprietà

Questa proprietà esegue una query sul decodificatore per la frequenza massima di fotogrammi completi supportati dal decodificatore. Il tipo di dati per questa proprietà è una **struttura \_ AM QueryRate.**

Questa proprietà è definita per la versione 1.1 di questo set di proprietà. vedere [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Etichetta | Valore |
|-------------------|---------------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange         |
| ID proprietà       | Am \_ RATE \_ QueryFullFrameRate - proprietà |
| Tipo di dati         | [**AM \_ QueryRate**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Commenti

Se la velocità di riproduzione supera la velocità massima del decodificatore, il filtro di origine invia gruppi di campioni continui separati da discontinuità. I timestamp passano attraverso le discontinuità. Il filtro di origine potrebbe eseguire questa operazione anche se la velocità di riproduzione rientra nella velocità massima del decodificatore, perché potrebbero esserci altri fattori, ad esempio l'I/O su disco, che limitano la velocità di riproduzione completa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostare la proprietà Rate Change**](rate-change-property-set.md)
</dt> </dl>

 

 




