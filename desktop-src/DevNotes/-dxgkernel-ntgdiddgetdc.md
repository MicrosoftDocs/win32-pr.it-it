---
description: Crea un contesto di dispositivo (DC) per la superficie specificata.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Funzione NtGdiDdGetDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126753"
---
# <a name="ntgdiddgetdc-function"></a>NtGdiDdGetDC (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Crea un contesto di dispositivo (DC) per la superficie specificata.

## <a name="syntax"></a>Sintassi


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ in\]
</dt> <dd>

Handle per una superficie DirectDraw in modalità kernel restituita in precedenza da [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) o [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).

</dd> <dt>

*puColorTable* \[ in\]
</dt> <dd>

Puntatore a una tabella dei colori di override per il controller di dominio restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, la funzione restituisce un **HDC** valido. in caso contrario, restituisce **null**.

## <a name="remarks"></a>Commenti

È consentito un solo controller di dominio per superficie in un determinato momento. Le chiamate successive a **NtGdiDdGetDC** avranno esito negativo finché non verrà rilasciato il controller di dominio precedente.

Si consiglia alle applicazioni di chiamare [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) , che fornisce la stessa funzionalità in modo indipendente dal sistema operativo.

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

[**DdGetDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
