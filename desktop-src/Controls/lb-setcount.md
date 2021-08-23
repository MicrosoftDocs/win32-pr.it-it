---
title: LB_SETCOUNT messaggio (Winuser.h)
description: Imposta il numero di elementi in una casella di riepilogo creata con lo stile LBS NODATA e non creata con lo stile \_ \_ HASSTRINGS di LBS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b3f68a67de2b7caa77cfd7c9e6f2a5b164e20af42100882fef1aad04eca14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433943"
---
# <a name="lb_setcount-message"></a>Messaggio \_ LB SETCOUNT

Imposta il numero di elementi in una casella di riepilogo creata con lo stile [**\_ LBS NODATA**](list-box-styles.md) e non creata con lo stile [**\_ HASSTRINGS di LBS.**](list-box-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il nuovo numero di elementi nella casella di riepilogo.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ ERR. Se la memoria non è sufficiente per archiviare gli elementi, il valore restituito è LB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Il **messaggio \_ LB SETCOUNT** è supportato solo dalle caselle di riepilogo create con lo stile [**\_ LBS NODATA**](list-box-styles.md) e non con lo stile [**\_ LBS HASSTRINGS.**](list-box-styles.md) Tutte le altre caselle di riepilogo restituiscono LB \_ ERR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ GETCOUNT**](lb-getcount.md)
</dt> </dl>

 

 





