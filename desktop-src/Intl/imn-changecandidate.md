---
description: Notifica all'applicazione quando un IME sta per modificare il contenuto della finestra candidata. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: IMN_CHANGECANDIDATE di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599f064b05f4fa0bda205825d623d13eec39334683fbe2b69f1c8b7b2997026b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949252"
---
# <a name="imn_changecandidate-notification-code"></a>Codice di \_ notifica IMN CHANGECANDIDATE

Notifica all'applicazione quando un IME sta per modificare il contenuto della finestra candidata. L'applicazione riceve questo comando tramite il [**messaggio WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ CHANGECANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Flag dell'elenco di candidati. Ogni bit corrisponde a un elenco di candidati: bit 0 al primo elenco, bit 1 al secondo elenco e così via. Se un bit specificato è 1, la finestra candidata corrispondente sta per essere modificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo comando se visualizza i candidati stessi.

La finestra IME modifica l'aspetto della finestra candidata quando elabora questo comando. Un'applicazione può ottenere informazioni sulla finestra di sistema con [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) e [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)

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

[**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[**NOTIFICA \_ IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




