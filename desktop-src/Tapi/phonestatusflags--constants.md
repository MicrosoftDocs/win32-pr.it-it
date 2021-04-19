---
description: Le \_ costanti del flag di bit PHONESTATUSFLAGS descrivono una serie di informazioni sullo stato dei dispositivi telefonici.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Costanti PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326144"
---
# <a name="phonestatusflags_-constants"></a>\_Costanti PHONESTATUSFLAGS

Le costanti del flag di bit **PHONESTATUSFLAGS \_** descrivono una serie di informazioni sullo stato dei dispositivi telefonici.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ connesso**
</dt> <dd> <dl> <dt>



Specifica se il telefono è attualmente connesso a TAPI. **True** se connesso; in caso contrario, **false** .


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ sospeso**
</dt> <dd> <dl> <dt>



Specifica se la manipolazione di TAPI del dispositivo telefonico viene sospesa. **True** se sospeso; in caso contrario, **false** . L'uso di un dispositivo telefonico da parte di un'applicazione può essere sospeso temporaneamente quando il Commuter vuole modificare il telefono in modo che non possa tollerare interferenze dall'applicazione.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




