---
description: Il metodo ConnectFrontEnd compila il front-end del grafico dei filtri dalla sequenza temporale corrente.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: Metodo IRenderEngine::ConnectFrontEnd (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7e0b00d467eb56dabaf6623f129ed1eb82945a1add63386b2b21fb01f725082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154038"
---
# <a name="irenderengineconnectfrontend-method"></a>Metodo IRenderEngine::ConnectFrontEnd

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `ConnectFrontEnd` metodo compila il front-end del grafico dei filtri dalla sequenza temporale corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori restituiti possibili sono i seguenti:



| Codice restituito                                                                                                  | Descrizione                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione completata.<br/>                                                            |
| <dl> <dt>**S \_ WARN \_ OUTPUTRESET**</dt> </dl>          | La parte di rendering del grafo è stata eliminata.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Nessuna sequenza temporale impostata per questo motore di rendering.<br/>                             |
| <dl> <dt>**E \_ DEVE \_ ESSERE INIT \_ RENDERER**</dt> </dl>       | Impossibile inizializzare il motore di rendering.<br/>                                 |
| <dl> <dt>**E \_ IL MOTORE DI RENDERING È \_ \_ \_ INTERROTTO**</dt> </dl> | L'operazione non è riuscita perché il rendering del progetto non è stato eseguito correttamente.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | Errore imprevisto.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | Tipo di supporto non valido.<br/>                                                 |



 

## <a name="remarks"></a>Commenti

Questo metodo non compila la parte di rendering del grafico di filtro. L'applicazione deve connettere i pin di output sul front-end ai filtri di rendering desiderati:

-   Per visualizzare l'anteprima, chiamare [**il metodo IRenderEngine::RenderOutputPins.**](irenderengine-renderoutputpins.md)
-   Per eseguire l'output di un file, chiamare [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) per recuperare il pin di output per ogni gruppo, quindi connettere i pin a un filtro multiplexer.

Se si usa il motore di rendering di base, i pin di output sul front-end producono dati non compressi. Se si usa il motore di rendering intelligente, i pin di output producono dati compressi.

Se si modifica la sequenza temporale dopo aver compilato il grafico dei filtri, è necessario chiamare di nuovo `ConnectFrontEnd` per ricompilare il front-end. Il metodo mantiene la parte di rendering del grafo quando possibile. Tuttavia, se si aggiunge o si elimina un gruppo o si modifica l'ordine dei gruppi, elimina la parte di rendering e l'applicazione `ConnectFrontEnd` deve ricompilarla. Se il metodo elimina la parte di rendering, restituisce S \_ WARN \_ OUTPUTRESET.

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

 

 




