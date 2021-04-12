---
description: Imposta il valore della chiave di colore per la superficie specificata.
ms.assetid: 052dba97-c047-4ef7-a908-2a66ade3af10
title: Funzione NtGdiDdSetColorKey (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetColorKey
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7d6186df13ee88ca3de4f123381c012548b1cd85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523002"
---
# <a name="ntgdiddsetcolorkey-function"></a>NtGdiDdSetColorKey (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Imposta il valore della chiave di colore per la superficie specificata.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdSetColorKey(
  _In_    HANDLE              hSurface,
  _Inout_ PDD_SETCOLORKEYDATA puSetColorKeyData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ in\]
</dt> <dd>

Puntatore alla struttura [**\_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie a cui deve essere associata la chiave di colore.

</dd> <dt>

*puSetColorKeyData* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**DD \_ SETCOLORKEYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) che contiene le informazioni necessarie per impostare la chiave di colore per la superficie specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdSetColorKey** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_driver DDHAL \_ gestito**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione. Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione. In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED driver \_ DDHAL**</dt> </dl> | Il driver non ha commenti sull'operazione richiesta. Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di livello inferiore grafica](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
