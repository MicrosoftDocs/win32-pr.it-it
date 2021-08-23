---
description: Consente al driver di specificare il numero di superfici provvisorie necessarie per supportare il GUID specificato e le dimensioni, la posizione e il formato di ognuna di queste superfici.
ms.assetid: 1f3207a8-aa6a-47a3-a1d0-19166592eeca
title: Funzione NtGdiDdGetMoCompBuffInfo (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetMoCompBuffInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4e2d324cf1b0b986845a7fab95c24abb9f44eb4c6024bbba9be101d25e1318a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956330"
---
# <a name="ntgdiddgetmocompbuffinfo-function"></a>Funzione NtGdiDdGetMoCompBuffInfo

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Consente al driver di specificare il numero di superfici provvisorie necessarie per supportare il GUID specificato e le dimensioni, la posizione e il formato di ognuna di queste superfici.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdGetMoCompBuffInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETMOCOMPCOMPBUFFDATA puGetBuffData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto DirectDraw in modalità kernel creato in precedenza.

</dd> <dt>

*puGetBuffData* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura \_ DD GETMOCOMPCOMPBUFFDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata) che contiene le informazioni sul buffer compresso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdGetMoCompBuffInfo** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ GESTITO**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione. Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione . In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt> </dl> | Il driver non ha commenti sull'operazione richiesta. Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione indipendente dal dispositivo DirectDraw o Direct3D.<br/> |



 

## <a name="remarks"></a>Commenti

Per altre informazioni, vedere Microsoft DirectX Video Acceleration Driver Development Kit (DDK).

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

 

 
