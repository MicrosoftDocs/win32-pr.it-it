---
description: Determina se si è verificato l'ultimo capovolgimento richiesto su una superficie.
ms.assetid: 4489e259-b22d-4e72-807a-5290401f0331
title: Funzione NtGdiDdGetFlipStatus (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetFlipStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4e309d5bdda6e6c18145a36902bd8b4927fab7c11bf314f88571c4f0de4b7dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956340"
---
# <a name="ntgdiddgetflipstatus-function"></a>Funzione NtGdiDdGetFlipStatus

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Determina se si è verificato l'ultimo capovolgimento richiesto su una superficie.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdGetFlipStatus(
  _In_    HANDLE                hSurface,
  _Inout_ PDD_GETFLIPSTATUSDATA puGetFlipStatusData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ Pollici\]
</dt> <dd>

Handle a una [struttura DD \_ SURFACE \_ LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di cui viene eseguita una query sullo stato di capovolgimento.

</dd> <dt>

*puGetFlipStatusData* \[ in, out\]
</dt> <dd>

Puntatore a [una struttura \_ DD GETFLIPSTATUSDATA](https://msdn.microsoft.com/library/ms793859.aspx) che contiene le informazioni necessarie per eseguire la query dello stato di capovolgimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdGetFlipStatus** restituisce uno dei codici di callback seguenti.



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

 

 




