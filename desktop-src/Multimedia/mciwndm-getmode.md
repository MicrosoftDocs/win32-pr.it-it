---
title: Messaggio di MCIWNDM_GETMODE (VFW. h)
description: Il \_ messaggio MCIWNDM GetMode recupera la modalità operativa corrente di un dispositivo MCI. I dispositivi MCI hanno diverse modalità operative, indicate da costanti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE messaggi multimediali di Windows
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
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118947"
---
# <a name="mciwndm_getmode-message"></a>\_Messaggio GETMODE MCIWNDM

Il messaggio **MCIWNDM \_ GetMode** recupera la modalità operativa corrente di un dispositivo MCI. I dispositivi MCI hanno diverse modalità operative, indicate da costanti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .


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

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntatore al buffer definito dall'applicazione utilizzato per restituire la modalità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un Integer che corrisponde alla costante MCI che definisce la modalità.

## <a name="remarks"></a>Commenti

Se la stringa con terminazione null che descrive la modalità è più lunga del buffer, viene troncata.

Non tutti i dispositivi possono funzionare in ogni modalità. Ad esempio, il dispositivo MCIAVI è un dispositivo di riproduzione; non supporta la modalità di registrazione. È possibile recuperare le modalità seguenti utilizzando **MCIWNDM \_ GetMode**.



| Modalità operativa | Costante MCI          |
|----------------|-----------------------|
| non pronto      | \_modalità MCI \_ non \_ pronta |
| apre           | \_modalità MCI \_ aperta       |
| in pausa         | \_sospensione della modalità MCI \_      |
| riproduzione in corso        | \_riproduzione in modalità MCI \_       |
| registrazione      | \_record in modalità MCI \_     |
| ricerca        | \_ricerca in modalità MCI \_       |
| Arrestato        | \_arresto modalità \_ MCI       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





