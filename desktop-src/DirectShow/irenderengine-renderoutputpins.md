---
description: Il metodo RenderOutputPins crea la parte di anteprima del grafico dei filtri.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: Metodo IRenderEngine::RenderOutputPins (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b81ea650d805c8ed2e42797f4dffdd9851eb3f072cff0abb05f54c4581684bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818563"
---
# <a name="irenderenginerenderoutputpins-method"></a>Metodo IRenderEngine::RenderOutputPins

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `RenderOutputPins` metodo crea la parte di anteprima del grafico dei filtri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce valori **HRESULT.** Di seguito sono indicati i valori possibili:



| Codice restituito                                                                                                  | Descrizione                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione completata.<br/>                                                        |
| <dl> <dt>**AUDIO VFW \_ NON \_ SOTTOPOSTO A \_ \_ RENDERING**</dt> </dl>  | Impossibile riprodurre il flusso audio.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argomento non valido.<br/>                                               |
| <dl> <dt>**E \_ IL MOTORE DI RENDERING È \_ \_ \_ INTERROTTO**</dt> </dl> | Operazione non riuscita perché il rendering del progetto non è stato eseguito correttamente.<br/> |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl>                 | Errore imprevisto.<br/>                                               |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafico. Per eseguire un'operazione diversa dall'anteprima, non chiamare questo metodo. Chiamare invece [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) per ottenere puntatori ai pin di output.

Se nel computer dell'utente non è presente alcuna scheda audio, questo metodo restituisce VFW \_ S \_ AUDIO NOT \_ \_ RENDERED. In questo caso non sarà disponibile l'anteprima audio, ma l'anteprima video non è influenzata.

Se il segnaposto è di un gruppo di video, questo metodo crea una finestra video. Il thread chiamante deve inviare messaggi, ad esempio per spostare la finestra o rispondere ai clic del mouse nell'area client della finestra.

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

 

 




