---
description: Causa l'intercambio della memoria della superficie associata alla destinazione e alle superfici correnti.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Funzione NtGdiDdFlip (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877741"
---
# <a name="ntgdiddflip-function"></a>NtGdiDdFlip (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Causa l'intercambio della memoria della superficie associata alla destinazione e alle superfici correnti.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurfaceCurrent* \[ in\]
</dt> <dd>

Handle per la [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie corrente.

</dd> <dt>

*hSurfaceTarget* \[ in\]
</dt> <dd>

Handle per la [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di destinazione, ovvero l'area in cui il driver deve essere invertito.

</dd> <dt>

*hSurfaceCurrentLeft* \[ in\]
</dt> <dd>

Handle per la [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di sinistra corrente.

</dd> <dt>

*hSurfaceTargetLeft* \[ in\]
</dt> <dd>

Handle per la [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di destinazione sinistra in cui eseguire il capovolgimento.

</dd> <dt>

*puFlipData* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [DD \_ FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) che contiene le informazioni necessarie per eseguire il capovolgimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdFlip** restituisce uno dei codici di callback seguenti.



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

 

 




