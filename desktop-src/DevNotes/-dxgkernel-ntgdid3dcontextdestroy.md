---
description: Elimina il contesto specificato.
ms.assetid: ac113178-bdb6-4601-940d-6b00b339904d
title: Funzione NtGdiD3DContextDestroy (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroy
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 46397237cd775fb28dd7b3b50e55fdc598fd4cff46eeffd69755b35fa87b9f44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636601"
---
# <a name="ntgdid3dcontextdestroy-function"></a>Funzione NtGdiD3DContextDestroy

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Elimina il contesto specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiD3DContextDestroy(
  _In_ LPD3DNTHAL_CONTEXTDESTROYDATA pContextDestroyData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContextDestroyData* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura D3DNTHAL \_ CONTEXTDESTROYDATA**](/windows-hardware/drivers/ddi/) che contiene le informazioni necessarie al driver per eliminare il contesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiD3DContextDestroy restituisce** uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ GESTITO**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione. Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione . In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt> </dl> | Il driver non ha alcun commento sull'operazione richiesta. Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

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

 

 
