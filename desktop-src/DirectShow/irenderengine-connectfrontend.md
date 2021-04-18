---
description: Il metodo ConnectFrontEnd compila il front-end del grafico di filtro dalla sequenza temporale corrente.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'Metodo IRenderEngine:: ConnectFrontEnd (qedit. h)'
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
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330396"
---
# <a name="irenderengineconnectfrontend-method"></a>Metodo IRenderEngine:: ConnectFrontEnd

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `ConnectFrontEnd` metodo compila il front-end del grafico di filtro dalla sequenza temporale corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Tra i possibili valori restituiti sono inclusi i seguenti:



| Codice restituito                                                                                                  | Descrizione                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>                                                            |
| <dl> <dt>**S \_ avvisa \_ OUTPUTRESET**</dt> </dl>          | Il rendering della parte del grafico è stato eliminato.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Nessuna sequenza temporale impostata per questo motore di rendering.<br/>                             |
| <dl> <dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt> </dl>       | Impossibile inizializzare il motore di rendering.<br/>                                 |
| <dl> <dt>**\_motore di rendering E \_ \_ \_ danneggiato**</dt> </dl> | L'operazione non è riuscita perché il rendering del progetto non è stato eseguito correttamente.<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>                 | Errore imprevisto.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | Tipo di supporto non valido.<br/>                                                 |



 

## <a name="remarks"></a>Commenti

Questo metodo non compila la parte di rendering del grafico del filtro. L'applicazione deve connettere i pin di output sul front-end ai filtri di rendering desiderati:

-   Per visualizzare l'anteprima, chiamare il metodo [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) .
-   Per restituire un file, chiamare [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) per recuperare il pin di output per ogni gruppo, quindi connettere i pin a un filtro multiplexer.

Se si usa il motore di rendering di base, i pin di output sul front-end producono dati non compressi. Se si usa il motore di rendering intelligente, i pin di output producono dati compressi.

Se si modifica la sequenza temporale dopo aver compilato il grafico del filtro, è necessario chiamare `ConnectFrontEnd` di nuovo per ricompilare il front-end. Il metodo conserva la parte di rendering del grafo quando possibile. Tuttavia, se si aggiunge o Elimina un gruppo o si modifica l'ordine dei gruppi, `ConnectFrontEnd` Elimina la parte di rendering e l'applicazione deve ricompilarla. Se il metodo elimina la parte di rendering, restituisce S \_ WARN \_ OUTPUTRESET.

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

 

 




