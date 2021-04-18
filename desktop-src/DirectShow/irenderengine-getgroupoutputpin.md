---
description: Il metodo GetGroupOutputPin Recupera il pin di output per il gruppo specificato.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'Metodo IRenderEngine:: GetGroupOutputPin (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330394"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>Metodo IRenderEngine:: GetGroupOutputPin

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetGroupOutputPin` metodo recupera il pin di output per il gruppo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gruppo* 
</dt> <dd>

Indice in base zero che specifica il gruppo.

</dd> <dt>

*ppRenderPin* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I possibili valori sono i seguenti:



| Codice restituito                                                                                                  | Descrizione                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | Il gruppo non ha un pin di output.<br/>                              |
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argomento non valido.<br/>                                               |
| <dl> <dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt> </dl>       | Impossibile inizializzare il motore di rendering.<br/>                             |
| <dl> <dt>**\_puntatore E**</dt> </dl>                    | Puntatore non valido.<br/>                                                |
| <dl> <dt>**\_motore di rendering E \_ \_ \_ danneggiato**</dt> </dl> | L'operazione non è riuscita perché il rendering del progetto non è stato eseguito correttamente.<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>                 | Errore imprevisto.<br/>                                               |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafo. Ogni gruppo rappresenta un singolo flusso multimediale e il front-end ha un pin di output corrispondente.

È possibile utilizzare questo metodo per creare la parte di rendering di un grafo di scrittura di file. Connettere i pin di output ai filtri multiplexer e ai filtri del writer di file. Per ulteriori informazioni, vedere [rendering di un progetto](rendering-a-project.md).

Per l'anteprima, non è necessario chiamare questo metodo. È sufficiente chiamare **ConnectFrontEnd** seguito da [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).

Se il metodo restituisce S \_ OK, l'interfaccia **Ipin** restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

 

 




