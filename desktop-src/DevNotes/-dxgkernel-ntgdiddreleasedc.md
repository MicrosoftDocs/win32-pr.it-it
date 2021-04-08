---
description: Rilascia il contesto di dispositivo creato in precedenza per l'oggetto Surface Microsoft DirectDraw in modalità kernel indicato.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Funzione NtGdiDdReleaseDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877261"
---
# <a name="ntgdiddreleasedc-function"></a>NtGdiDdReleaseDC (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Rilascia il contesto di dispositivo creato in precedenza per l'oggetto Surface Microsoft DirectDraw in modalità kernel indicato.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ in\]
</dt> <dd>

Handle per l'oggetto Surface DirectDraw in modalità kernel creato in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Le applicazioni che devono ottenere un controller di dominio per una superficie DirectDraw possono utilizzare [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), che espone questa funzionalità in modo indipendente dal sistema operativo.

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

[**DdReleaseDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
