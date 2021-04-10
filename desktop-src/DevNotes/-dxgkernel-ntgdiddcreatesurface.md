---
description: Connette una superficie a un'altra superficie.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Funzione NtGdiDdCreateSurface (Ntgdi. h)
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
ms.openlocfilehash: 663d29be32dc544d44a47061e1a6ff7f81e60862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125946"
---
# <a name="ntgdiddcreatesurface-function"></a>NtGdiDdCreateSurface (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Connette una superficie a un'altra superficie.

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

*hDirectDraw* \[ in\]
</dt> <dd>

Handle per la [**struttura \_ \_ globale di DIRECTDRAW DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) che rappresenta il driver.

</dd> <dt>

*hSurface* \[ in\]
</dt> <dd>

Handle precedente alla stessa superficie. Utilizzato se la superficie viene ricreata dopo un'opzione di modalità.

</dd> <dt>

*puSurfaceDescription* \[ in uscita\]
</dt> <dd>

Puntatore alla struttura [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) che descrive la superficie o il buffer che deve essere creato dal driver.

</dd> <dt>

*puSurfaceGlobalData* \[ in uscita\]
</dt> <dd>

Puntatore alla struttura [**\_ \_ globale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) contenente i dati di superficie condivisi globalmente con più superfici.

</dd> <dt>

*puSurfaceLocalData* \[ in uscita\]
</dt> <dd>

Puntatore a un elenco di [**strutture \_ \_ locali della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrivono gli oggetti Surface creati dal driver.

</dd> <dt>

*puSurfaceMoreData* \[ in uscita\]
</dt> <dd>

Puntatore a una [**\_ superficie DD \_ più**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) struttura che contiene dati della superficie locale aggiuntivi.

</dd> <dt>

*puCreateSurfaceData* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) che contiene le informazioni necessarie per creare una superficie.

</dd> <dt>

*puhSurface* \[ out\]
</dt> <dd>

Viene usato dall'API DirectDraw e non deve essere compilato dal driver.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdCreateSurface** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_driver DDHAL \_ gestito**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione. Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione. In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED driver \_ DDHAL**</dt> </dl> | Il driver non ha commenti sull'operazione richiesta. Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

## <a name="remarks"></a>Commenti

È consigliabile che l'applicazione chiami [IDirectDraw7:: CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) anziché usare questa funzione.

Quando si crea una catena di superfici collegate, ad esempio una catena di scambio o una catena o mipmap, è necessario chiamare [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) per ogni superficie. Chiamare quindi [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) per collegarli. Infine, chiamare **NtGdiDdCreateSurface** per la prima superficie della catena. In questo caso, *hSurface* è l'handle restituito da **NtGdiDdCreateSurfaceObject** per la prima superficie della catena.

**NtGdiDdCreateSurface** deve essere chiamato solo per creare superfici nella memoria video locale e non locale. Non deve mai essere chiamata per creare superfici di memoria di sistema. Per creare le superfici di memoria di sistema, usare invece [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) .

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

 

 
