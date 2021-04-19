---
description: Restituisce l'handle dell'API Microsoft DirectX in modalità kernel da usare nelle chiamate successive ai punti di ingresso in modalità kernel che controllano il meccanismo dell'API DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Funzione NtGdiDdGetDxHandle (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304846"
---
# <a name="ntgdiddgetdxhandle-function"></a>NtGdiDdGetDxHandle (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Restituisce l'handle dell'API Microsoft DirectX in modalità kernel da usare nelle chiamate successive ai punti di ingresso in modalità kernel che controllano il meccanismo dell'API DirectX.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ in\]
</dt> <dd>

Handle per l'oggetto DirectDraw proprietario della superficie. Questo parametro è facoltativo e può essere impostato su **null**.

</dd> <dt>

*hSurface* \[ in\]
</dt> <dd>

Handle per la superficie per cui restituire un handle dell'API DirectX in modalità kernel. Questo parametro è facoltativo e può essere impostato su **null**.

</dd> <dt>

*bRelease* \[ in\]
</dt> <dd>

Impostare su **true** se l'interfaccia della modalità kernel dell'API DirectX deve essere rilasciata. In caso contrario, **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Handle di API DirectX usato nei successivi punti di ingresso del kernel basati sull'API DirectX.

## <a name="remarks"></a>Commenti

Se vengono specificati sia *hDirectDraw* che *hSurface* , *hSurface* viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di livello inferiore grafica](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




