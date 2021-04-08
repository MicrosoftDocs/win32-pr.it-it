---
description: Indica a una finestra IME di impostare la posizione della finestra candidati. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: Comando IMC_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ac05890e4c720c5b671faa7f20a68a96b24a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752346"
---
# <a name="imc_setcandidatepos-command"></a>\_Comando SETCANDIDATEPOS IMC

Indica a una finestra IME di impostare la posizione della finestra candidati. Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMC \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a una struttura [**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) che contiene la coordinata x e la coordinata y per la finestra candidati. L'applicazione deve impostare il membro **dwIndex** della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.

## <a name="remarks"></a>Commenti

Questo comando è destinato alle applicazioni che visualizzano i caratteri di composizione autonomamente, ma usano la finestra IME per visualizzare i candidati.

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

[**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**\_controllo IME \_ WM**](wm-ime-control.md)
</dt> </dl>

 

 




