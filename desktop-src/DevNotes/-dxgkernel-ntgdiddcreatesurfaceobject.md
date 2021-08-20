---
description: Crea un oggetto superficie in modalità kernel che rappresenta l'oggetto superficie in modalità utente a cui fa riferimento puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Funzione NtGdiDdCreateSurfaceObject (Ntgdi.h)
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
ms.openlocfilehash: 7dac10cb5f648cc7281d95bcd83be9983a63abd76208f6f745e1bd6c5ec00b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956540"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>Funzione NtGdiDdCreateSurfaceObject

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Crea un oggetto superficie in modalità kernel che rappresenta l'oggetto superficie in modalità utente a cui fa riferimento *puSurfaceLocal.*

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

*hDirectDrawLocal* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto DirectDraw in modalità kernel.

</dd> <dt>

*hSurface* \[ Pollici\]
</dt> <dd>

Handle precedente alla stessa superficie. Usato se la superficie viene ri-creata dopo un cambio di modalità.

</dd> <dt>

*puSurfaceLocal* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta l'oggetto superficie in modalità utente DirectDraw a cui associare la memoria allocata. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puSurfaceMore* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura DD \_ SURFACE \_ MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) che contiene dati locali aggiuntivi per ogni singolo oggetto superficie. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puSurfaceGlobal* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura DD \_ SURFACE \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) che contiene dati di superficie condivisi a livello globale con più superfici. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*bComplete* \[ Pollici\]
</dt> <dd>

Flag di completamento dell'oggetto in modalità kernel. Può essere uno dei valori seguenti.

<dt>



 (TRUE)


</dt> <dd>

Completare tutte le elaborazioni relative alla rappresentazione in modalità kernel.

</dd> <dt>



 (FALSE)


</dt> <dd>

Creare l'oggetto , ma non configurare dati interni, ad esempio il puntatore alla memoria. Gli oggetti creati usando **FALSE** possono essere collegati tramite [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) e vengono completati da una chiamata a [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questa funzione restituisce un handle per la rappresentazione della superficie in modalità kernel. in caso contrario, restituisce **NULL.**

## <a name="remarks"></a>Commenti

Si consiglia alle applicazioni di usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) per creare e gestire oggetti dispositivo grafico. Questi costrutti astrarre il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.

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

[**DdCreateSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**NtGdiDdDeleteSurfaceObject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
