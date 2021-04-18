---
description: "Il metodo SetRenderRange2 imposta l'intervallo di tempo nella sequenza temporale di cui eseguire il rendering. Questo metodo è equivalente a IRenderEngine:: SetRenderRange, ma accetta valori di tipo Double."
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'Metodo IRenderEngine:: SetRenderRange2 (qedit. h)'
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
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330783"
---
# <a name="irenderenginesetrenderrange2-method"></a>Metodo IRenderEngine:: SetRenderRange2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetRenderRange2` metodo imposta l'intervallo di tempo nella sequenza temporale di cui eseguire il rendering. Questo metodo è equivalente a [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md), ma accetta valori di tipo **Double**.

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

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>                            |
| <dl> <dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




