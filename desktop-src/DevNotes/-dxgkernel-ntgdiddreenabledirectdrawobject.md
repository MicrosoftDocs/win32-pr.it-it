---
description: Ri abilita un oggetto dispositivo in modalità kernel Microsoft DirectDraw dopo un cambio di modalità.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Funzione NtGdiDdReenableDirectDrawObject (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 808e2e74492b9a3e828e09389e04f0e1e4b09fef9a63fdd7a22d81521b3df30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045571"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>Funzione NtGdiDdReenableDirectDrawObject

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Ri abilita un oggetto dispositivo in modalità kernel Microsoft DirectDraw dopo un cambio di modalità.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDrawLocal* \[ Pollici\]
</dt> <dd>

Oggetto DirectDraw che deve essere ri-abilitato.

</dd> <dt>

*pubNewMode* \[ in, out\]
</dt> <dd>

Puntatore a un oggetto BOOL che verrà riempito con un valore che indica se la modalità di visualizzazione è stata modificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo (il dispositivo può essere ri-abilitato), questa funzione restituisce **TRUE.** In caso contrario( ad esempio, il driver di visualizzazione è stato modificato), restituisce **FALSE**.

## <a name="remarks"></a>Commenti

Dopo che l'oggetto è stato ri-abilitato, è possibile rieseguire query sulle funzionalità del dispositivo tramite una chiamata a [**NtGdiDdQueryDirectDrawObject.**](-dxgkernel-ntgdiddquerydirectdrawobject.md)

Si consiglia alle applicazioni di usare le API DirectDraw o [Direct3D](../direct3d10/d3d10-graphics-reference.md) versione 8, che automatizzano e astrarno questo processo in modo indipendente dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di basso livello per grafica](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReenableDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
