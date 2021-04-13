---
title: Messaggio di MCIWNDM_GETLENGTH (VFW. h)
description: Il \_ messaggio MCIWNDM GetLength recupera la lunghezza del contenuto o del file attualmente utilizzato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475527"
---
# <a name="mciwndm_getlength-message"></a>\_Messaggio MCIWNDM GETlength

Il messaggio **MCIWNDM \_ GetLength** recupera la lunghezza del contenuto o del file attualmente utilizzato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce la lunghezza. Le unità per la lunghezza dipendono dal formato dell'ora corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





