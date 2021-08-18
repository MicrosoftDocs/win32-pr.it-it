---
description: Restituisce l'handle dell'API Microsoft DirectX in modalità kernel da usare nelle chiamate successive ai punti di ingresso in modalità kernel che controllano il meccanismo dell'API DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Funzione NtGdiDdGetDxHandle (Ntgdi.h)
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
ms.openlocfilehash: 13234c7ebe350f096164f0a5de0bde7a60e819e80899aa87258a76727855b869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331921"
---
# <a name="ntgdiddgetdxhandle-function"></a>Funzione NtGdiDdGetDxHandle

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

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

*hDirectDraw* \[ Pollici\]
</dt> <dd>

Handle all'oggetto DirectDraw proprietario dell'area. Questo parametro è facoltativo e può essere impostato su **NULL.**

</dd> <dt>

*hSurface* \[ Pollici\]
</dt> <dd>

Handle alla superficie per cui restituire un handle dell'API DirectX in modalità kernel. Questo parametro è facoltativo e può essere impostato su **NULL.**

</dd> <dt>

*bRelease* \[ Pollici\]
</dt> <dd>

Impostare su **TRUE se** deve essere rilasciata l'interfaccia in modalità kernel dell'API DirectX. In caso contrario, **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Handle dell'API DirectX usato nei punti di ingresso del kernel orientati all'API DirectX successivi.

## <a name="remarks"></a>Commenti

Se vengono *specificati sia hDirectDraw* che *hSurface,* *hSurface* viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di basso livello per grafica](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




