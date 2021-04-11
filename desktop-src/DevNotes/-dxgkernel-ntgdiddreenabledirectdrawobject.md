---
description: Abilita nuovamente un oggetto dispositivo in modalità kernel di Microsoft DirectDraw dopo un'opzione di modalità.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Funzione NtGdiDdReenableDirectDrawObject (Ntgdi. h)
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
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127283"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>NtGdiDdReenableDirectDrawObject (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Abilita nuovamente un oggetto dispositivo in modalità kernel di Microsoft DirectDraw dopo un'opzione di modalità.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDrawLocal* \[ in\]
</dt> <dd>

Oggetto DirectDraw che deve essere riabilitato.

</dd> <dt>

*pubNewMode* \[ in uscita\]
</dt> <dd>

Puntatore a un BOOL che verrà riempito con un valore che indica se la modalità di visualizzazione è cambiata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo (il dispositivo può essere riabilitato), questa funzione restituisce **true**. In caso contrario (ad esempio, il driver di visualizzazione è stato modificato), restituisce **false**.

## <a name="remarks"></a>Commenti

Una volta che l'oggetto è stato riabilitato, è possibile eseguire una nuova query sulle funzionalità del dispositivo tramite una chiamata a [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).

Per le applicazioni è consigliabile usare le API DirectDraw o [Direct3D](../direct3d10/d3d10-graphics-reference.md) versione 8, che automatizzano ed astraggono questo processo in modo indipendente dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di livello inferiore grafica](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReenableDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
