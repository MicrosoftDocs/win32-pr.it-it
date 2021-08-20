---
description: Le costanti del flag di bit PHONESTATUSFLAGS \_ descrivono un'ampia gamma di informazioni sullo stato del dispositivo telefonico.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: PHONESTATUSFLAGS_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b42f8e13adfae54c56e44244d04b3961216edb87e29730fec6f689f315380a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060649"
---
# <a name="phonestatusflags_-constants"></a>Costanti PHONESTATUSFLAGS \_

Le costanti del flag di bit **PHONESTATUSFLAGS \_** descrivono un'ampia gamma di informazioni sullo stato del dispositivo telefonico.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ CONNECTED**
</dt> <dd> <dl> <dt>



Specifica se il telefono è attualmente connesso a TAPI. **TRUE se** connesso, **FALSE in caso** contrario.


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ SOSPESO**
</dt> <dd> <dl> <dt>



Specifica se la manipolazione tapI del dispositivo telefonico è sospesa. **TRUE se** sospeso, **FALSE in caso contrario.** L'uso di un dispositivo telefonico da parte di un'applicazione può essere temporaneamente sospeso quando il commutatore vuole modificare il telefono in modo che non possa tollerare interferenze dall'applicazione.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




