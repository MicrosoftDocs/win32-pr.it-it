---
title: Metodo GetMode IWMPSettings
description: Il metodo GetMode restituisce un valore che indica se la modalità ciclo o shuffle è attiva.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- Metodo GetMode Windows Media Player
- Metodo GetMode Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, metodo GetMode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327480"
---
# <a name="iwmpsettingsgetmode-method"></a>Metodo IWMPSettings:: GetMode

Il metodo **GetMode** restituisce un valore che indica se la modalità ciclo o shuffle è attiva.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrMode* \[ in\]
</dt> <dd>

**System. String** che corrisponde a uno dei valori seguenti.



| Valore      | Descrizione                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| riavvolgimento rapido | Le tracce vengono riavviate dall'inizio dopo la riproduzione fino alla fine.                                |
| loop       | La sequenza di tracce si ripete.                                                           |
| showFrame  | Il fotogramma chiave più vicino viene visualizzato in caso di mancata riproduzione. Questa modalità non è pertinente per le tracce audio. |
| shuffle    | Le tracce vengono riprodotte in ordine casuale.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore **System. Boolean** che indica se la modalità specificata è attiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. semode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





