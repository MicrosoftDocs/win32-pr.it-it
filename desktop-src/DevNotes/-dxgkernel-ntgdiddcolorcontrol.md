---
description: Controlla i controlli di luminosità e luminanza di una superficie sovrapposta.
ms.assetid: 2f617c89-5505-4d84-be7d-473b216c0571
title: Funzione NtGdiDdColorControl (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdColorControl
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5e83dba1dcdc46fb4715fbbdcb6a5ed009f77cf29212e65be9b0270ba01a55e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956710"
---
# <a name="ntgdiddcolorcontrol-function"></a>Funzione NtGdiDdColorControl

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Controlla i controlli di luminosità e luminanza di una superficie sovrapposta.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdColorControl(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_COLORCONTROLDATA puColorControlData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ Pollici\]
</dt> <dd>

Handle alla struttura [**DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta la superficie di sovrapposizione.

</dd> <dt>

*puColorControlData* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura \_ COLORCONTROLDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) che contiene le informazioni sul controllo dei colori per una superficie di sovrapposizione specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdColorControl** restituisce uno dei codici di callback seguenti.



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

 

 
