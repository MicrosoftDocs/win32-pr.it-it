---
description: Indica a una finestra IME di impostare la posizione della finestra dei candidati. Per inviare questo comando, l'applicazione usa il messaggio WM \_ IME \_ CONTROL con le impostazioni dei parametri illustrate di seguito.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: IMC_SETCANDIDATEPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fbce21cac53eecf3ad5b99cc7dbe5cf5b52304ed25869a5c3f6ae729ac9d016
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107271"
---
# <a name="imc_setcandidatepos-command"></a>Comando IMC \_ SETCANDIDATEPOS

Indica a una finestra IME di impostare la posizione della finestra dei candidati. Per inviare questo comando, l'applicazione usa il [**messaggio WM \_ IME \_ CONTROL**](wm-ime-control.md) con le impostazioni dei parametri illustrate di seguito.


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMC \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a [**una struttura CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) che contiene la coordinata x e la coordinata y per la finestra candidata. L'applicazione deve impostare **il membro dwIndex** di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo oppure un valore diverso da zero in caso contrario.

## <a name="remarks"></a>Commenti

Questo comando è destinato alle applicazioni che visualizzano i caratteri di composizione in modo proprio, ma usano la finestra IME per visualizzare i candidati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Imm.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodi di input](input-method-manager.md)
</dt> <dt>

[Comandi di Gestione metodi di input](input-method-manager-commands.md)
</dt> <dt>

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**CONTROLLO \_ IME \_ WM**](wm-ime-control.md)
</dt> </dl>

 

 




