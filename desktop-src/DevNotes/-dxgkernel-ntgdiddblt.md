---
description: Esegue un trasferimento a blocchi di bit.
ms.assetid: 90cc02af-96af-4913-ae7d-62f39cd6ddd7
title: Funzione NtGdiDdBlt (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBlt
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f0f4ae51663e9d1c398c34708520047f43288c1f571458a879e262ec9fca025d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911957"
---
# <a name="ntgdiddblt-function"></a>Funzione NtGdiDdBlt

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Esegue un trasferimento a blocchi di bit.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdBlt(
  _In_    HANDLE      hSurfaceDest,
  _In_    HANDLE      hSurfaceSrc,
  _Inout_ PDD_BLTDATA puBltData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurfaceDest* \[ Pollici\]
</dt> <dd>

Handle a una [**struttura DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie su cui eseguire il blit.

</dd> <dt>

*hSurfaceSrc* \[ Pollici\]
</dt> <dd>

Handle a una [**struttura DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie di origine.

</dd> <dt>

*puBltData* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura \_ BLTDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) che contiene le informazioni necessarie al driver per eseguire il blit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdBlt** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ GESTITO**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione. Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione . In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt> </dl> | Il driver non ha alcun commento sull'operazione richiesta. Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

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

 

 
