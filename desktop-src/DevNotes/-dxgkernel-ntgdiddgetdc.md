---
description: Crea un contesto di dispositivo (DC) per la superficie specificata.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Funzione NtGdiDdGetDC (Ntgdi.h)
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
ms.openlocfilehash: 200635ca71ab16a84a137f85be13cc4fdbb6db200e4c0da795d07f945f06e9f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053341"
---
# <a name="ntgdiddgetdc-function"></a>Funzione NtGdiDdGetDC

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

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

*hSurface* \[ Pollici\]
</dt> <dd>

Handle a una superficie DirectDraw in modalità kernel restituita in precedenza da [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) o [**NtGdiDdCreateSurfaceObject.**](-dxgkernel-ntgdiddcreatesurfaceobject.md)

</dd> <dt>

*puColorTable* \[ Pollici\]
</dt> <dd>

Puntatore a una tabella dei colori di override per il controller di dominio restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questa funzione restituisce un oggetto **HDC valido.** In caso contrario, **restituisce NULL.**

## <a name="remarks"></a>Commenti

È consentito un solo controller di dominio per ogni superficie in un determinato momento. Le chiamate successive a **NtGdiDdGetDC** avranno esito negativo fino al rilascio del controller di dominio precedente.

È consigliabile che le applicazioni chiamino [invece IDirectDrawSurface7::GetDC,](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) che fornisce la stessa funzionalità in modo indipendente dal sistema operativo.

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

[**DdGetDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
