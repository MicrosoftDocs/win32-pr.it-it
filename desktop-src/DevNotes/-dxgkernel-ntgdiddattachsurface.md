---
description: Collega due rappresentazioni di superficie in modalità kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Funzione NtGdiDdAttachSurface (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8ec07f539cfa2a99338d8366f10f7c3d79dbdd5ef26a6de0ee0296941e2c84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088031"
---
# <a name="ntgdiddattachsurface-function"></a>Funzione NtGdiDdAttachSurface

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Collega due rappresentazioni di superficie in modalità kernel.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurfaceFrom* \[ Pollici\]
</dt> <dd>

Handle all'oggetto surface in modalità kernel che sarà il punto iniziale del nuovo allegato.

</dd> <dt>

*hSurfaceTo* \[ Pollici\]
</dt> <dd>

Handle all'oggetto surface in modalità kernel che sarà il punto finale del nuovo allegato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdAttachSurface** restituisce uno degli elementi seguenti:



| Codice restituito                                                                          | Descrizione                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | La chiamata di funzione è riuscita.<br/> |
| <dl> <dt>**False**</dt> </dl> | Chiamata di funzione non riuscita.<br/>    |



 

## <a name="remarks"></a>Commenti

Per una descrizione completa degli allegati di superficie, vedere DirectDraw Software Development Kit (SDK) e Driver Development Kit (DDK).

> [!Note]  
> Come per altri allegati di superficie, l'allegato risultante è unidiredato. Dopo la chiamata a questa funzione, *hSurfaceTo* non verrà associato a *hSurfaceFrom*.

 

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

 

 




