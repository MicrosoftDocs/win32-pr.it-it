---
description: Crea un oggetto Surface in modalità kernel che rappresenta l'oggetto Surface della modalità utente a cui fa riferimento puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Funzione NtGdiDdCreateSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049107"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>NtGdiDdCreateSurfaceObject (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Crea un oggetto Surface in modalità kernel che rappresenta l'oggetto Surface della modalità utente a cui fa riferimento *puSurfaceLocal*.

## <a name="syntax"></a>Sintassi


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDrawLocal* \[ in\]
</dt> <dd>

Handle per l'oggetto DirectDraw in modalità kernel.

</dd> <dt>

*hSurface* \[ in\]
</dt> <dd>

Handle precedente alla stessa superficie. Utilizzato se la superficie viene ricreata dopo un'opzione di modalità.

</dd> <dt>

*puSurfaceLocal* \[ in\]
</dt> <dd>

Puntatore alla struttura [**\_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta l'oggetto superficie in modalità utente di DirectDraw a cui associare la memoria allocata. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puSurfaceMore* \[ in\]
</dt> <dd>

Puntatore alla [**superficie DD \_ \_ più**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) struttura che contiene dati locali aggiuntivi per ogni singolo oggetto Surface. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puSurfaceGlobal* \[ in\]
</dt> <dd>

Puntatore alla struttura [**\_ \_ globale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) che contiene i dati di superficie condivisi a livello globale con più superfici. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*bComplete* \[ in\]
</dt> <dd>

Flag di completamento oggetto in modalità kernel. Può essere uno dei valori seguenti.

<dt>



 TRUE


</dt> <dd>

Completa tutte le operazioni di elaborazione relative alla rappresentazione in modalità kernel.

</dd> <dt>



 FALSE


</dt> <dd>

Creare l'oggetto, ma non impostare dati interni come il puntatore di memoria. Gli oggetti creati usando **false** possono essere collegati usando [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) e vengono completati da una chiamata a [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questa funzione restituisce un handle alla rappresentazione di superficie in modalità kernel; in caso contrario, restituisce **null**.

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

[**DdCreateSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**NtGdiDdDeleteSurfaceObject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
