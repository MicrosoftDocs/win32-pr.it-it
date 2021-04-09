---
description: Crea una superficie Microsoft Direct3D da una superficie Microsoft DirectDraw e vi associa un valore di handle richiesto.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Funzione NtGdiDdCreateSurfaceEx (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125940"
---
# <a name="ntgdiddcreatesurfaceex-function"></a>NtGdiDdCreateSurfaceEx (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. In alternativa, usare i DirectDraw e Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Crea una superficie Microsoft Direct3D da una superficie Microsoft DirectDraw e vi associa un valore di handle richiesto.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ in\]
</dt> <dd>

Handle per l'oggetto DirectDraw creato dall'applicazione.

</dd> <dt>

*hSurface* \[ in\]
</dt> <dd>

Handle per la superficie DirectDraw da creare per Direct3D. Questi handle sono univoci all'interno di ogni struttura [**\_ \_ locale di DIRECTDRAW GG**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) diversa.

</dd> <dt>

*dwSurfaceHandle* \[ in\]
</dt> <dd>

Handle per una struttura [**DD \_ CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) che contiene le informazioni necessarie per la creazione della superficie da parte del driver.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdCreateSurfaceEx** restituisce uno dei codici di callback seguenti.



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

 

 
