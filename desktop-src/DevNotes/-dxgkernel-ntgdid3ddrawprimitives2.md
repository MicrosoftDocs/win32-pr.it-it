---
description: Esegue il rendering delle primitive e restituisce lo stato di rendering aggiornato.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: Funzione NtGdiD3DDrawPrimitives2 (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049127"
---
# <a name="ntgdid3ddrawprimitives2-function"></a>NtGdiD3DDrawPrimitives2 (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Esegue il rendering delle primitive e restituisce lo stato di rendering aggiornato.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCmdBuf* \[ in\]
</dt> <dd>

Handle per la [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che identifica la superficie DirectDraw contenente i dati del comando.

</dd> <dt>

*hVBuf* \[ in\]
</dt> <dd>

Handle per la [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che identifica la superficie DirectDraw contenente i dati del vertice.

</dd> <dt>

*pded* \[ in uscita\]
</dt> <dd>

Puntatore a una [**struttura \_ DRAWPRIMITIVES2DATA di D3DNTHAL**](/windows-hardware/drivers/ddi/) contenente le informazioni necessarie per il rendering di una o più primitive da parte del driver.

</dd> <dt>

*pfpVidMemCmd* \[ in uscita\]
</dt> <dd>

Nuovo puntatore alla memoria video se il driver ha invertito il buffer dei comandi.

</dd> <dt>

*pdwSizeCmd* \[ in uscita\]
</dt> <dd>

Specifica il numero minimo di byte in base ai quali il driver deve aumentare il buffer dei comandi di swapping.

</dd> <dt>

*pfpVidMemVtx* \[ in uscita\]
</dt> <dd>

Nuovo puntatore alla memoria video se il driver ha invertito il buffer del vertice.

</dd> <dt>

*pdwSizeVtx* \[ in uscita\]
</dt> <dd>

Specifica il numero minimo di byte che il driver deve allocare per il buffer dei vertici di swapping.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiD3DDrawPrimitives2** restituisce uno dei codici di callback seguenti.



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

 

 
