---
title: MCM_SETUNICODEFORMAT messaggio (Commctrl.h)
description: 'MCM_SETUNICODEFORMAT messaggio: imposta il flag di formato carattere Unicode per il controllo.'
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- MCM_SETUNICODEFORMAT di windows del messaggio
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa922b0dde8702f447690f9626938364174cbff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112370"
---
# <a name="mcm_setunicodeformat-message"></a>Messaggio \_ DI MCM SETUNICODEFORMAT

Imposta il flag di formato carattere Unicode per il controllo . Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ MonthCal SetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Determina il set di caratteri utilizzato dal controllo . Se questo valore è diverso da zero, il controllo userà caratteri Unicode. Se questo valore è zero, il controllo userà caratteri ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode precedente per il controllo.

## <a name="remarks"></a>Commenti

Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCM \_ GETUNICODEFORMAT**](mcm-getunicodeformat.md)
</dt> </dl>

 

 





