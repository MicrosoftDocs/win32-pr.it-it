---
title: Metodo IWMPSettings getMode
description: Il metodo getMode restituisce un valore che indica se la modalità ciclo o la modalità casuale è attiva.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- Metodo getMode Windows Media Player
- Metodo getMode Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, metodo getMode
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
ms.openlocfilehash: fae5d910dbbdf1fc2241a63dcf6c61c94e968cf0f2b36316407aafc8fc5f2dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246301"
---
# <a name="iwmpsettingsgetmode-method"></a>Metodo IWMPSettings::getMode

Il **metodo getMode** restituisce un valore che indica se la modalità ciclo o la modalità casuale è attiva.

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

*bstrMode* \[ Pollici\]
</dt> <dd>

**System.String** che è uno dei valori seguenti.



| Valore      | Descrizione                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| riavvolgimento automatico | Le tracce vengono riavviate dall'inizio dopo la riproduzione fino alla fine.                                |
| loop       | La sequenza di tracce si ripete.                                                           |
| showFrame  | Il fotogramma chiave più vicino viene visualizzato quando non viene riprodotto. Questa modalità non è rilevante per le tracce audio. |
| shuffle    | Le tracce vengono riprodotte in ordine casuale.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore **System.Boolean** che indica se la modalità specificata è attiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.setMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





