---
description: "Funzione NtGdiDdCreateSurface: collega una superficie a un'altra superficie."
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Funzione NtGdiDdCreateSurface (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085779"
---
# <a name="ntgdiddcreatesurface-function"></a>Funzione NtGdiDdCreateSurface

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Collega una superficie a un'altra superficie.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ Pollici\]
</dt> <dd>

Handle per la [**struttura \_ DD DIRECTDRAW \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) che rappresenta il driver.

</dd> <dt>

*hSurface* \[ Pollici\]
</dt> <dd>

Handle precedente alla stessa superficie. Usato se la superficie viene ri-creata dopo un cambio di modalità.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Puntatore alla [**struttura DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) che descrive la superficie o il buffer che il driver deve creare.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Puntatore alla [**struttura DD \_ SURFACE \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) contenente i dati di superficie condivisi a livello globale con più superfici.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Puntatore a un elenco [**di strutture \_ SURFACE \_ LOCAL DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrivono gli oggetti superficie creati dal driver.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura DD \_ SURFACE \_ MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) che contiene dati aggiuntivi sulla superficie locale.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura \_ CREATESURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) che contiene le informazioni necessarie per creare una superficie.

</dd> <dt>

*puhSurface* \[ Cambio\]
</dt> <dd>

Viene usato dall'API DirectDraw e non deve essere compilato dal driver.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdCreateSurface** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ GESTITO**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione. Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione . In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt> </dl> | Il driver non ha alcun commento sull'operazione richiesta. Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

## <a name="remarks"></a>Commenti

È consigliabile che l'applicazione [chiami IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) anziché usare questa funzione.

Quando si crea una catena di superfici collegate, ad esempio una catena di scambio o una catena o mipmap, è prima necessario chiamare [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) per ogni superficie. Chiamare quindi [**NtGdiDdAttachSurface per**](-dxgkernel-ntgdiddattachsurface.md) collegarli. Chiamare infine **NtGdiDdCreateSurface solo** per la prima superficie della catena. In questo caso, *hSurface* è l'handle restituito da **NtGdiDdCreateSurfaceObject** per la prima superficie della catena.

**NtGdiDdCreateSurface** deve essere chiamato solo per creare superfici nella memoria video locale e non locale. Non deve mai essere chiamato per creare superfici di memoria di sistema. Per creare superfici di memoria di sistema, usare [**NtGdiDdCreateSurfaceObject.**](-dxgkernel-ntgdiddcreatesurfaceobject.md)

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

 

 
