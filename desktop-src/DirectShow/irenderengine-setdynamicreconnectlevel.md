---
description: Il metodo SetDynamicReconnectLevel imposta il livello di riconnessione dinamica durante il rendering.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: Metodo IRenderEngine::SetDynamicReconnectLevel (Qedit.h)
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
ms.openlocfilehash: b43967753dd03d213a322ce569d113346542a57b5f37fd69fc28937198109049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083681"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>Metodo IRenderEngine::SetDynamicReconnectLevel

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

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

Combinazione [**di flag di riconnessione**](dynamic-reconnection-flags.md)dinamica, che specifica il livello di riconnessione dinamica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                               | Descrizione                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione completata.<br/>         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Non implementato.<br/> |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il motore di rendering di base carica ogni origine prima di eseguire il rendering di un progetto. Ciò può comportare un lungo tempo di avvio. Con la riconnessione dinamica, le origini vengono caricate solo quando necessario. Ciò può ridurre il tempo di avvio, ma può interferire con la riproduzione senza problemi. In genere, più clip di origine vengono utilizzate da un progetto, più si potrebbe trarre vantaggio dalla riconnessione dinamica.

Il motore di rendering intelligente non implementa questo metodo.

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

 

 




