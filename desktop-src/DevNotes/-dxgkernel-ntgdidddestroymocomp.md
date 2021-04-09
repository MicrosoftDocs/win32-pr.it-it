---
description: Notifica al driver che questo oggetto compensazione movimento non verrà più utilizzato. Il driver deve ora eseguire tutte le operazioni di pulizia necessarie.
ms.assetid: 1d86a564-efe1-4971-99ec-2c9a6aa59c89
title: Funzione NtGdiDdDestroyMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: b7bc5915fe43bd4d48495b2b1beda8ee38f05fe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877558"
---
# <a name="ntgdidddestroymocomp-function"></a>NtGdiDdDestroyMoComp (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Notifica al driver che questo oggetto compensazione movimento non verrà più utilizzato. Il driver deve ora eseguire tutte le operazioni di pulizia necessarie.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdDestroyMoComp(
  _In_    HANDLE                hMoComp,
  _Inout_ PDD_DESTROYMOCOMPDATA puBeginFrameData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMoComp* \[ in\]
</dt> <dd>

Handle per una [**struttura \_ \_ locale DD MOTIONCOMP**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) che contiene una descrizione dell'oggetto compensazione movimento da eliminare definitivamente.

</dd> <dt>

*puBeginFrameData* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**DD \_ DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) che contiene le informazioni necessarie per completare la compensazione del movimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdDestroyMoComp** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_driver DDHAL \_ gestito**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione. Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione. In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED driver \_ DDHAL**</dt> </dl> | Il driver non ha commenti sull'operazione richiesta. Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

## <a name="remarks"></a>Commenti

Per ulteriori informazioni, vedere Microsoft DirectX Video Acceleration Driver Development Kit (DDK).

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

 

 
