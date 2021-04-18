---
description: Il metodo SetDynamicReconnectLevel imposta il livello di riconnessione dinamica durante il rendering.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'Metodo IRenderEngine:: SetDynamicReconnectLevel (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330790"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>Metodo IRenderEngine:: SetDynamicReconnectLevel

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetDynamicReconnectLevel` metodo imposta il livello di riconnessione dinamica durante il rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Level* 
</dt> <dd>

Combinazione di [**flag di riconnessione dinamici**](dynamic-reconnection-flags.md), che specificano il livello di riconnessione dinamica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                               | Descrizione                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Esito positivo.<br/>         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Non implementato.<br/> |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il motore di rendering di base carica ogni origine prima di eseguire il rendering di un progetto. Questo può comportare un lungo periodo di avvio. Con la riconnessione dinamica, le origini vengono caricate solo quando necessario. Questo può ridurre il tempo di avvio, ma potrebbe interferire con la riproduzione uniforme. In genere, maggiore è il numero di clip di origine utilizzate da un progetto, più si può trarre vantaggio dalla riconnessione dinamica.

Il motore di rendering intelligente non implementa questo metodo.

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

 

 




