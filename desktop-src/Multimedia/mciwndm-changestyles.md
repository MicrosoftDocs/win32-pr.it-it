---
title: MCIWNDM_CHANGESTYLES messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ CHANGESTYLES modifica gli stili usati dalla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5525066f4c377cc093e1e7a0dedd4edf7463792c136214a519da9744917cbc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525511"
---
# <a name="mciwndm_changestyles-message"></a>MESSAGGIO CHANGESTYLES DI MCIWNDM \_

Il **messaggio MCIWNDM \_ CHANGESTYLES** modifica gli stili usati dalla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndChangeStyles.**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*Maschera*
</dt> <dd>

Maschera che identifica gli stili che è possibile modificare. Questa maschera è l'operatore OR bit per bit di tutti gli stili a cui sarà consentito modificare.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valore*
</dt> <dd>

Nuove impostazioni di stile per la finestra. Specificare zero per questo parametro per disattivare tutti gli stili identificati nella maschera. Per un elenco degli stili disponibili, vedere la [**funzione MCIWndCreate.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





