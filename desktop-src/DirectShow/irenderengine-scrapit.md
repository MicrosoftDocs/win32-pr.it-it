---
description: Il metodo ScrapIt rimuove il grafico di filtro del motore di rendering e tutti gli oggetti associati.
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: 'Metodo IRenderEngine:: ScrapIt (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f9febbe20cfd5ab9a6577a6e00989c7d6fc4145
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332746"
---
# <a name="irenderenginescrapit-method"></a>Metodo IRenderEngine:: ScrapIt

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `ScrapIt` metodo rimuove il grafico di filtro del motore di rendering e tutti gli oggetti associati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

 

 




