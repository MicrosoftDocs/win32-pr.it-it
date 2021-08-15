---
description: Il metodo SetRenderRange2 imposta l'intervallo di tempo sulla sequenza temporale di cui eseguire il rendering. Questo metodo equivale a IRenderEngine::SetRenderRange, ma accetta valori di tipo double.
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: Metodo IRenderEngine::SetRenderRange2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a81d186ac648d2dcf617def0069c486b888e791c301cb45d4661e95b44dcbc25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397572"
---
# <a name="irenderenginesetrenderrange2-method"></a>Metodo IRenderEngine::SetRenderRange2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `SetRenderRange2` metodo imposta l'intervallo di tempo sulla sequenza temporale di cui eseguire il rendering. Questo metodo equivale a [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md), ma accetta valori di tipo **double**.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Inizia* 
</dt> <dd>

Ora di inizio, in secondi.

</dd> <dt>

*Stop* 
</dt> <dd>

Tempo di arresto, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>                            |
| <dl> <dt>**E \_ DEVE \_ INIT \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




