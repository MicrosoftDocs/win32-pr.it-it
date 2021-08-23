---
description: Consente di creare un comando a livello di driver o un vertex buffer della descrizione specificata.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: Funzione NtGdiDdCreateD3DBuffer (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 55e28e50f10ced5380685cbdb5016363a77adc7e61d2df201565d18f4794fcf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956700"
---
# <a name="ntgdiddcreated3dbuffer-function"></a>Funzione NtGdiDdCreateD3DBuffer

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Consente di creare un comando a livello di driver o un vertex buffer della descrizione specificata.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ Pollici\]
</dt> <dd>

Handle per la [**struttura \_ DD DIRECTDRAW \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) che rappresenta il driver.

</dd> <dt>

*hSurface* \[ in, out\]
</dt> <dd>

Puntatore a una matrice di handle di superficie. Il chiamante può impostare questi handle ai valori di handle precedenti se le superfici vengono ri create dopo un cambio di modalità. Questo processo è denominato "ripristino" nella documentazione di DirectDraw.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) che descrive la superficie o il buffer che il driver deve creare.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura \_ DD SURFACE \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) contenente dati di superficie condivisi a livello globale con più superfici.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Puntatore a un elenco [**di strutture \_ SURFACE \_ LOCAL DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrivono gli oggetti superficie creati dal driver. In genere è presente una sola voce in questa matrice.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura DD \_ SURFACE \_ MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) che contiene dati aggiuntivi sulla superficie locale.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura \_ CREATESURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) che contiene le informazioni necessarie per creare il buffer.

</dd> <dt>

*puhSurface* \[ in, out\]
</dt> <dd>

Viene usato dall'API DirectDraw e non deve essere compilato dal driver.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdCreateD3DBuffer** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ GESTITO**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione. Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione . In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt> </dl> | Il driver non ha commenti sull'operazione richiesta. Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione indipendente dal dispositivo DirectDraw o Direct3D.<br/> |



 

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

 

 
