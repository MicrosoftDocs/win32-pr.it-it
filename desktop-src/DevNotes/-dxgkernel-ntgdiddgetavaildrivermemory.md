---
description: Esegue una query sulla quantità di memoria disponibile in tutti gli heap di memoria video.
ms.assetid: 6718e8da-0da0-42e3-a02b-6884b141fe24
title: Funzione NtGdiDdGetAvailDriverMemory (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetAvailDriverMemory
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4c2a66c174538c128185b2e8d4939a76d50a4ba6d3aff4347e7a6e0af9b4f549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956380"
---
# <a name="ntgdiddgetavaildrivermemory-function"></a>Funzione NtGdiDdGetAvailDriverMemory

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Esegue una query sulla quantità di memoria disponibile in tutti gli heap di memoria video.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdGetAvailDriverMemory(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_GETAVAILDRIVERMEMORYDATA puGetAvailDriverMemoryData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto DirectDraw in modalità kernel creato in precedenza.

</dd> <dt>

*puGetAvailDriverMemoryData* \[ in, out\]
</dt> <dd>

Puntatore a [una struttura \_ DD GETAVAILDRIVERMEMORYDATA](https://msdn.microsoft.com/library/ms794088.aspx) che contiene le informazioni necessarie per eseguire la query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdGetAvailDriverMemory** restituisce uno dei codici di callback seguenti.



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

 

 




