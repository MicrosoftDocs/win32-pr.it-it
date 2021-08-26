---
description: Indica a una finestra IME di ottenere la posizione della finestra candidata. Per inviare questo comando, l'applicazione usa il messaggio WM \_ IME \_ CONTROL con le impostazioni dei parametri illustrate di seguito.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: IMC_GETCANDIDATEPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e155a08c9d95fa2ac9f865d80b18d51120d19b28489bcad418eb4323dda39c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107321"
---
# <a name="imc_getcandidatepos-command"></a>Comando IMC \_ GETCANDIDATEPOS

Indica a una finestra IME di ottenere la posizione della finestra candidata. Per inviare questo comando, l'applicazione usa il [**messaggio WM \_ IME \_ CONTROL**](wm-ime-control.md) con le impostazioni dei parametri illustrate di seguito.


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMC \_ GETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a [**una struttura CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) che contiene la posizione della finestra candidata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo oppure un valore diverso da zero in caso contrario.

## <a name="remarks"></a>Commenti

Poiché l'IME potrebbe modificare la posizione di una finestra candidata, un'applicazione usa questo comando per ottenere la posizione effettiva per decidere se riposizionare la finestra. La posizione recuperata si trova nelle coordinate della finestra rispetto alla finestra con lo stato attivo per l'input corrente.

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
</dt> </dl>

 

 




