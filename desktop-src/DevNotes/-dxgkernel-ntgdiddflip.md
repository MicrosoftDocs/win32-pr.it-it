---
description: Fa sì che la memoria della superficie associata alle superfici di destinazione e correnti sia intercambiata.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Funzione NtGdiDdFlip (Ntgdi.h)
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
ms.openlocfilehash: 18113c841c22b31c9768d42491a63ead8cafee3c3b598bc46f442068592e67b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956490"
---
# <a name="ntgdiddflip-function"></a>Funzione NtGdiDdFlip

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Fa sì che la memoria della superficie associata alle superfici di destinazione e correnti sia intercambiata.

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

*hSurfaceCurrent* \[ Pollici\]
</dt> <dd>

Handle alla struttura [DD \_ SURFACE \_ LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie corrente.

</dd> <dt>

*hSurfaceTarget* \[ Pollici\]
</dt> <dd>

Handle alla struttura [DD \_ SURFACE \_ LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di destinazione, ovvero la superficie su cui il driver deve capovolgere.

</dd> <dt>

*hSurfaceCurrentLeft* \[ Pollici\]
</dt> <dd>

Handle alla struttura [DD \_ SURFACE \_ LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie sinistra corrente.

</dd> <dt>

*hSurfaceTargetLeft* \[ Pollici\]
</dt> <dd>

Handle alla struttura [DD \_ SURFACE \_ LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di destinazione sinistra su cui capovolgere.

</dd> <dt>

*puFlipData* \[ in, out\]
</dt> <dd>

Puntatore a [una struttura \_ DD FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) che contiene le informazioni necessarie per eseguire lo scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdFlip** restituisce uno dei codici di callback seguenti.



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

 

 




