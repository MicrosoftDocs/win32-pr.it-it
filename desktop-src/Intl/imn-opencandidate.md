---
description: Notifica a un'applicazione quando un IME sta per aprire la finestra candidata. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: IMN_OPENCANDIDATE evento (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf6db7415a62b6d77925a4fb7106b70f0b42d77f922e0c1b6df76e71d10c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147634"
---
# <a name="imn_opencandidate-event"></a>Evento IMN \_ OPENCANDIDATE

Notifica a un'applicazione quando un IME sta per aprire la finestra candidata. L'applicazione riceve questo comando tramite il [**messaggio WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ OPENCANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Flag dell'elenco di candidati. Ogni bit corrisponde a un elenco di candidati: bit 0 al primo elenco, bit 1 al secondo e così via. Se un bit specificato è 1, la finestra candidata corrispondente sta per essere aperta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo comando se visualizza i candidati stessi. L'applicazione può recuperare un elenco di candidati da visualizzare usando la [**funzione ImmGetCandidateList.**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)

Per impostazione predefinita, la finestra IME crea una finestra candidata quando elabora questo comando.

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

[**NOTIFICA \_ IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




