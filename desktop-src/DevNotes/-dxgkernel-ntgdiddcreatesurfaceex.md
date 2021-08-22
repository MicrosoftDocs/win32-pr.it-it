---
description: Crea una superficie Microsoft Direct3D da una superficie Microsoft DirectDraw e associa un valore di handle richiesto.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Funzione NtGdiDdCreateSurfaceEx (Ntgdi.h)
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
ms.openlocfilehash: ff5db8859cc339dc97f86e1b0421f662d69b85ba0f46449a1e721c1dc355d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956560"
---
# <a name="ntgdiddcreatesurfaceex-function"></a>Funzione NtGdiDdCreateSurfaceEx

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece DirectDraw e Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Crea una superficie Microsoft Direct3D da una superficie Microsoft DirectDraw e associa un valore di handle richiesto.

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

*hDirectDraw* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto DirectDraw creato dall'applicazione.

</dd> <dt>

*hSurface* \[ Pollici\]
</dt> <dd>

Handle per l'area DirectDraw da creare per Direct3D. Questi handle sono univoci all'interno di [**ogni struttura \_ DD DIRECTDRAW \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) diversa.

</dd> <dt>

*dwSurfaceHandle* \[ Pollici\]
</dt> <dd>

Handle a una [**struttura \_ CREATESURFACEEXDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) che contiene le informazioni necessarie al driver per creare la superficie.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdCreateSurfaceEx** restituisce uno dei codici di callback seguenti.



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

 

 
