---
description: Crea un contesto.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: Funzione NtGdiD3DContextCreate (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: a11ae1d1e9b9469f22971ec3fc7447d8552b6d263bb43f4a8fe336ccbbc37a69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017739"
---
# <a name="ntgdid3dcontextcreate-function"></a>Funzione NtGdiD3DContextCreate

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Crea un contesto.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDrawLocal* \[ Pollici\]
</dt> <dd>

Handle a un oggetto DirectDraw in modalità kernel, creato in precedenza con [**NtGdiDdCreateDirectDrawObject,**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)che rappresenta il dispositivo in cui deve essere creato il contesto Direct3D.

</dd> <dt>

*hSurfColor* \[ Pollici\]
</dt> <dd>

Handle a una [**struttura DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie DirectDraw da usare come destinazione di rendering.

</dd> <dt>

*hSurfZ* \[ Pollici\]
</dt> <dd>

Handle a una [**struttura DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie DirectDraw da usare come buffer di profondità. Se questo membro è **NULL,** non deve essere eseguito alcun buffering di profondità.

</dd> <dt>

*pdcci* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura D3DNTHAL \_ CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) che contiene le informazioni necessarie per creare un contesto e i dati che il driver deve archiviare nel nuovo contesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiD3DContextCreate** restituisce uno dei codici di callback seguenti.



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

 

 
