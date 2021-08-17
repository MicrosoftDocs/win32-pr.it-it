---
description: Esegue una query sullo stato di blit della superficie specificata.
ms.assetid: 0221bdc6-2146-4f4d-afb5-d1f701446d5e
title: Funzione NtGdiDdGetBltStatus (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetBltStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 488d0b28da747346b795ef7a1c5a3846d4661c0afb31c65a9e624584b8fe60e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956360"
---
# <a name="ntgdiddgetbltstatus-function"></a>Funzione NtGdiDdGetBltStatus

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Esegue una query sullo stato di blit della superficie specificata.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdGetBltStatus(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_GETBLTSTATUSDATA puGetBltStatusData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ Pollici\]
</dt> <dd>

Handle a una [struttura SURFACE \_ \_ LOCAL DD](https://msdn.microsoft.com/library/ms793861.aspx) che rappresenta la superficie di cui viene eseguita una query sullo stato di blit.

</dd> <dt>

*puGetBltStatusData* \[ in, out\]
</dt> <dd>

Puntatore a [una struttura \_ GETBLTSTATUSDATA DD](https://msdn.microsoft.com/library/ms794243.aspx) che contiene le informazioni necessarie per eseguire la query sullo stato del blit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdGetBltStatus** restituisce uno dei codici di callback seguenti.



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

 

 




