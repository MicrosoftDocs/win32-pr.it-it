---
description: Questa funzione Abilita o Disabilita il supporto per i caratteri definiti dall'utente finale (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC (funzione)
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
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978631"
---
# <a name="enableeudc-function"></a>EnableEUDC (funzione)

Questa funzione Abilita o Disabilita il supporto per i caratteri definiti dall'utente finale (EUDC).

## <a name="syntax"></a>Sintassi


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fEnableEUDC* \[ in\]
</dt> <dd>

Valore booleano impostato su **true** per abilitare EUDC e su **false** per disabilitare EUDC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Se EUDC è disabilitato, il tentativo di visualizzare i caratteri EUDC provocherà glifi mancanti o errati.

Durante la multisessione, questa funzione influiscono solo sulla sessione corrente.

Si consiglia di utilizzare questa funzione con Windows XP SP2 o versione successiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Libreria<br/>                  | <dl> <dt>Gdi32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




