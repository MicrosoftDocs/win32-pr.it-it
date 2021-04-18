---
description: NtGdiDdDeleteSurfaceObject Elimina un oggetto Surface in modalità kernel creato in precedenza.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: Funzione NtGdiDdDeleteSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03988b842aacc29915287490508eb9e9d057e907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304461"
---
# <a name="ntgdidddeletesurfaceobject-function"></a>NtGdiDdDeleteSurfaceObject (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

**NtGdiDdDeleteSurfaceObject** Elimina un oggetto Surface in modalità kernel creato in precedenza.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ in\]
</dt> <dd>

Handle per l'oggetto Surface in modalità kernel creato in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Per creare e gestire oggetti dispositivo di grafica, è consigliabile usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) . Questi costrutti astraggono il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.

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

[**DdDeleteSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
