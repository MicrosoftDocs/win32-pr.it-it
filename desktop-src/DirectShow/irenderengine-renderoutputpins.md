---
description: Il metodo RenderOutputPins crea la parte in anteprima del grafico del filtro.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'Metodo IRenderEngine:: RenderOutputPins (qedit. h)'
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
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330791"
---
# <a name="irenderenginerenderoutputpins-method"></a>Metodo IRenderEngine:: RenderOutputPins

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `RenderOutputPins` metodo crea la parte in anteprima del grafico del filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce valori **HRESULT** . Di seguito sono indicati i valori possibili:



| Codice restituito                                                                                                  | Descrizione                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>                                                        |
| <dl> <dt>**\_non è \_ stato \_ eseguito il rendering dell'audio di \_ VFW**</dt> </dl>  | Non è possibile riprodurre il flusso audio.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argomento non valido.<br/>                                               |
| <dl> <dt>**\_motore di rendering E \_ \_ \_ danneggiato**</dt> </dl> | L'operazione non è riuscita perché il rendering del progetto non è stato eseguito correttamente.<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>                 | Errore imprevisto.<br/>                                               |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafo. Per eseguire un'operazione diversa dall'anteprima, non chiamare questo metodo. In alternativa, chiamare [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) per ottenere i puntatori ai pin di output.

Se non è presente alcuna scheda audio nel computer dell'utente, questo metodo restituisce l'audio VFW non sottoposto a \_ \_ \_ \_ rendering. In questo caso non sarà presente un'anteprima audio, ma l'anteprima video non è interessata.

Se il PIN è da un gruppo video, questo metodo crea una finestra video. Il thread chiamante deve inviare messaggi, ad esempio per spostare la finestra o rispondere ai clic del mouse nell'area client della finestra.

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

 

 




