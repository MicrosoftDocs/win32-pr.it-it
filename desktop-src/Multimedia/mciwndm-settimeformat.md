---
title: MCIWNDM_SETTIMEFORMAT messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ SETTIMEFORMAT imposta il formato dell'ora di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o usando la macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT di Windows multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79620aecba07b11ed63dfc43fd2d70b41728586b36649b4b13aace9d1364197c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802895"
---
# <a name="mciwndm_settimeformat-message"></a>Messaggio MCIWNDM \_ SETTIMEFORMAT

Il **messaggio MCIWNDM \_ SETTIMEFORMAT imposta** il formato dell'ora di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MCIWndSetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntatore a un buffer contenente la stringa con terminazione Null che indica il formato dell'ora. Specificare "frames" per impostare il formato dell'ora su frames o "ms" per impostare il formato dell'ora su millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Un'applicazione può specificare formati di ora diversi da fotogrammi o millisecondi purché i formati siano supportati dal dispositivo MCI. I formati non contigui, ad esempio tracce e SMPTE, possono causare un comportamento non sistematico del trackbar. Per questi formati di ora, è possibile disattivare la barra degli strumenti usando la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) e specificando lo stile della finestra MCIWNDF \_ NOPLAYBAR.

Se si vuole impostare il formato dell'ora su fotogrammi o millisecondi, è anche possibile usare la macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) o [**MCIWndUseTime.**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) Per un elenco dei formati di ora, vedere la macro [**MCIWndGetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





