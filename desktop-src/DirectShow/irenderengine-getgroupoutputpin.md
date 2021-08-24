---
description: Il metodo GetGroupOutputPin recupera il pin di output per il gruppo specificato.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: Metodo IRenderEngine::GetGroupOutputPin (Qedit.h)
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
ms.openlocfilehash: 99a1f3c60dcafdda219dc8a05f5523d7c2386249ff500bbb9abb463294ca7239
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767151"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>Metodo IRenderEngine::GetGroupOutputPin

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

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

*ppRenderPin* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I possibili valori sono i seguenti:



| Codice restituito                                                                                                  | Descrizione                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | Il gruppo non dispone di un pin di output.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione completata.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argomento non valido.<br/>                                               |
| <dl> <dt>**E \_ DEVE \_ ESSERE INIT \_ RENDERER**</dt> </dl>       | Impossibile inizializzare il motore di rendering.<br/>                             |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>                    | Puntatore non valido.<br/>                                                |
| <dl> <dt>**E \_ IL MOTORE DI RENDERING È \_ \_ \_ INTERROTTO**</dt> </dl> | L'operazione non è riuscita perché il rendering del progetto non è stato eseguito correttamente.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | Errore imprevisto.<br/>                                               |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafo. Ogni gruppo rappresenta un singolo flusso multimediale e il front-end ha un pin di output corrispondente.

È possibile usare questo metodo per creare la parte di rendering di un grafo di scrittura di file. Connessione pin di output ai filtri multiplexer e ai filtri writer di file. Per altre informazioni, vedere [Rendering di un Project](rendering-a-project.md).

Per l'anteprima, non è necessario chiamare questo metodo. È sufficiente **chiamare ConnectFrontEnd** seguito da [**IRenderEngine::RenderOutputPins.**](irenderengine-renderoutputpins.md)

Se il metodo restituisce S \_ OK, **l'interfaccia IPin** restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

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

 

 




