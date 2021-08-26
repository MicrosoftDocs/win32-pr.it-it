---
description: Consente al driver di segnalare che alloca internamente memoria di visualizzazione per eseguire la compensazione del movimento.
ms.assetid: cf2878ae-7eff-4214-bb9e-e8b608831108
title: Funzione NtGdiDdGetInternalMoCompInfo (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetInternalMoCompInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 323c6d36284032f5d9fb1ee73b90393ed3d00c0c8247002c1f8b0f42484784fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103861"
---
# <a name="ntgdiddgetinternalmocompinfo-function"></a>Funzione NtGdiDdGetInternalMoCompInfo

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Consente al driver di segnalare che alloca internamente memoria di visualizzazione per eseguire la compensazione del movimento.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdGetInternalMoCompInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETINTERNALMOCOMPDATA puGetInternalData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ Pollici\]
</dt> <dd>

Handle all'oggetto DirectDraw in modalità kernel creato in precedenza.

</dd> <dt>

*puGetInternalData* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura \_ DD GETINTERNALMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) che contiene i requisiti di memoria interna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdGetInternalMoCompInfo** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ GESTITO**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione. Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione . In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt> </dl> | Il driver non ha alcun commento sull'operazione richiesta. Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

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

 

 
