---
description: Riposiziona o modifica gli attributi visivi di una superficie di sovrapposizione.
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: Funzione NtGdiDdUpdateOverlay (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c65e906529e8afa11f2a16a1171c1d4a7c31ae29bac70d8200997b7a7b88a131
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108941"
---
# <a name="ntgdiddupdateoverlay-function"></a>Funzione NtGdiDdUpdateOverlay

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Riposiziona o modifica gli attributi visivi di una superficie di sovrapposizione.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurfaceDestination* \[ Pollici\]
</dt> <dd>

Handle all'oggetto DirectDraw in modalità kernel creato in precedenza.

</dd> <dt>

*hSurfaceSource* \[ Pollici\]
</dt> <dd>

Handle a una [**struttura DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie di sovrapposizione.

</dd> <dt>

*puUpdateOverlayData* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura DD \_ UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) che contiene le informazioni necessarie per aggiornare la sovrimpressione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdUpdateOverlay** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ GESTITO**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione. Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione . In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt> </dl> | Il driver non ha alcun commento sull'operazione richiesta. Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione indipendente dal dispositivo DirectDraw o Direct3D.<br/> |



 

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

 

 
