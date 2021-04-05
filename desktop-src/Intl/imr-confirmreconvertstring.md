---
description: Notifica a un'applicazione quando l'IME deve modificare la struttura RECONVERTSTRING. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: Codice di notifica IMR_CONFIRMRECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756494"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>\_Codice di notifica CONFIRMRECONVERTSTRING di IMR

Notifica a un'applicazione quando l'IME deve modificare la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) . L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMR \_ CONFIRMRECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a una struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) dall'IME. Per altre informazioni, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se l'applicazione accetta la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) modificata. In caso contrario, il comando restituisce 0 e l'IME utilizza la struttura **RECONVERTSTRING** originale.

## <a name="remarks"></a>Commenti

L'applicazione compila la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) alla ricezione del comando [IMR \_ RECONVERTSTRING](imr-reconvertstring.md) .

Dopo che l'applicazione ha gestito [IMR \_ RECONVERTSTRING](imr-reconvertstring.md), è possibile che l'IME non modifichi la struttura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) . L'IME invia una \_ richiesta IME WM \_ con **IMR \_ CONFIRMRECONVERTSTRING** per confermare le modifiche apportate alla struttura **RECONVERTSTRING** . Se l'applicazione restituisce **true** per **IMR \_ CONFIRMRECONVERTSTRING**, l'IME genera una nuova stringa di composizione basata sulla struttura **RECONVERTSTRING** per il comando **IMR \_ CONFIRMRECONVERTSTRING** . Se l'applicazione restituisce **false** per **IMR \_ CONFIRMRECONVERTSTRING**, l'IME genera una nuova stringa di composizione basata sulla struttura **RECONVERTSTRING** originale specificata dall'applicazione nel \_ comando IMR RECONVERTSTRING.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Imm. h (Includi Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodo di input](input-method-manager.md)
</dt> <dt>

[Comandi di input Method Manager](input-method-manager-commands.md)
</dt> <dt>

[\_RECONVERTSTRING IMR](imr-reconvertstring.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_richiesta IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 




