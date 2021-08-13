---
title: MCIWNDM_GETMODE messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ GETMODE recupera la modalità operativa corrente di un dispositivo MCI. I dispositivi MCI hanno diverse modalità operative, designate da costanti. È possibile inviare questo messaggio in modo esplicito o usando la macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE di Windows multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645d7a660df8d22cb2adb70a775d5431eb31dc986b502bb4dbb36b1963ce06f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429271"
---
# <a name="mciwndm_getmode-message"></a>Messaggio MCIWNDM \_ GETMODE

Il **messaggio MCIWNDM \_ GETMODE** recupera la modalità operativa corrente di un dispositivo MCI. I dispositivi MCI hanno diverse modalità operative, designate da costanti. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MCIWndGetMode.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Dimensione, in byte, del buffer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntatore al buffer definito dall'applicazione utilizzato per restituire la modalità .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un intero corrispondente alla costante MCI che definisce la modalità.

## <a name="remarks"></a>Commenti

Se la stringa con terminazione Null che descrive la modalità è più lunga del buffer, viene troncata.

Non tutti i dispositivi possono funzionare in ogni modalità. Ad esempio, il dispositivo MCIAVI è un dispositivo di riproduzione. non supporta la modalità di registrazione. Le modalità seguenti possono essere recuperate **usando MCIWNDM \_ GETMODE.**



| Modalità operativa | Costante MCI          |
|----------------|-----------------------|
| non pronto      | MODALITÀ MCI \_ \_ NON \_ PRONTA |
| apre           | MODALITÀ MCI \_ \_ APERTA       |
| in pausa         | SOSPENSIONE DELLA MODALITÀ MCI \_ \_      |
| riproduzione in corso        | RIPRODUZIONE IN MODALITÀ MCI \_ \_       |
| registrazione      | RECORD IN MODALITÀ MCI \_ \_     |
| ricerca        | MCI \_ MODE \_ SEEK       |
| Arrestato        | ARRESTO DELLA MODALITÀ MCI \_ \_       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





