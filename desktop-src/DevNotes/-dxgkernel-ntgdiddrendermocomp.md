---
description: Indica al driver quali macroblock eseguire il rendering specificando le superfici contenenti i macroblock, gli offset in ogni superficie in cui sono presenti i macroblock e le dimensioni dei dati dei macroblock di cui eseguire il rendering.
ms.assetid: c49d9dfa-a3db-4572-a474-72c7d4e80940
title: Funzione NtGdiDdRenderMoComp (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdRenderMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: d057ba1c7b533d75ce10754670b911ddc01a689acee29d79614a3ce2f273d278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827972"
---
# <a name="ntgdiddrendermocomp-function"></a>Funzione NtGdiDdRenderMoComp

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Indica al driver quali macroblock eseguire il rendering specificando le superfici contenenti i macroblock, gli offset in ogni superficie in cui sono presenti i macroblock e le dimensioni dei dati dei macroblock di cui eseguire il rendering.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdRenderMoComp(
  _In_    HANDLE               hMoComp,
  _Inout_ PDD_RENDERMOCOMPDATA puRenderMoCompData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMoComp* \[ Pollici\]
</dt> <dd>

Handle a una [**struttura DD \_ MOTIONCOMP \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) che contiene una descrizione della compensazione del movimento richiesta.

</dd> <dt>

*puRenderMoCompData* \[ in, out\]
</dt> <dd>

Puntatore a [**una struttura \_ DD RENDERMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) che contiene le informazioni necessarie per eseguire il rendering di un frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdRenderMoComp** restituisce uno dei codici di callback seguenti.



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

 

 
