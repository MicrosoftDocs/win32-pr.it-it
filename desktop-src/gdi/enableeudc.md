---
description: Questa funzione abilita o disabilita il supporto per i caratteri definiti dall'utente finale (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: Funzione EnableEUDC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 5767be62d23e992223500bf7192fc89efe04f03288280c73445378e083cc1613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699476"
---
# <a name="enableeudc-function"></a>Funzione EnableEUDC

Questa funzione abilita o disabilita il supporto per i caratteri definiti dall'utente finale (EUDC).

## <a name="syntax"></a>Sintassi


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fEnableEUDC* \[ Pollici\]
</dt> <dd>

Valore booleano impostato su **TRUE per** abilitare EUDC e **su FALSE** per disabilitare EUDC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Se EUDC è disabilitato, il tentativo di visualizzare i caratteri EUDC causa la mancanza o la mancata visualizzazione di glifi.

Durante più sessioni, questa funzione influisce solo sulla sessione corrente.

È consigliabile usare questa funzione con Windows XP SP2 o versione successiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Libreria<br/>                  | <dl> <dt>Gdi32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




