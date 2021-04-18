---
description: Connette due rappresentazioni di superficie in modalità kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Funzione NtGdiDdAttachSurface (Ntgdi. h)
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
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304568"
---
# <a name="ntgdiddattachsurface-function"></a>NtGdiDdAttachSurface (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Connette due rappresentazioni di superficie in modalità kernel.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurfaceFrom* \[ in\]
</dt> <dd>

Handle per l'oggetto Surface in modalità kernel che sarà il punto iniziale del nuovo allegato.

</dd> <dt>

*hSurfaceTo* \[ in\]
</dt> <dd>

Handle per l'oggetto Surface in modalità kernel che corrisponderà al punto finale del nuovo allegato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdAttachSurface** restituisce uno dei seguenti elementi:



| Codice restituito                                                                          | Descrizione                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | La chiamata di funzione è riuscita.<br/> |
| <dl> <dt>**FALSE**</dt> </dl> | Chiamata di funzione non riuscita.<br/>    |



 

## <a name="remarks"></a>Commenti

Per una descrizione completa degli allegati della superficie, vedere il Software Development Kit di DirectDraw (SDK) e il kit di sviluppo di driver (DDK).

> [!Note]  
> Come per gli altri allegati della superficie, l'allegato risultante è unidirezionale. Dopo la chiamata a questa funzione, *hSurfaceTo* non verrà associato a *hSurfaceFrom*.

 

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

 

 




