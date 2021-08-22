---
title: Metodo setMode IWMPSettings
description: Il metodo setMode imposta la modalità loop o shuffle su attiva o inattiva.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- Metodo setMode Windows Media Player
- Metodo setMode Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, metodo setMode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529aadf412cdae869ae3c308d82dcd08a7dfd581aeb7ecc711052f6acd54b962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568408"
---
# <a name="iwmpsettingssetmode-method"></a>Metodo IWMPSettings::setMode

Il **metodo setMode** imposta la modalità loop o shuffle su attiva o inattiva.

## <a name="syntax"></a>Sintassi


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrMode* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nome della modalità da modificare, contenente uno dei valori seguenti.



| Valore      | Descrizione                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| riavvolgimento automatico | Le tracce vengono riavviate dall'inizio dopo la riproduzione fino alla fine.                                |
| loop       | La sequenza di tracce si ripete.                                                           |
| showFrame  | Il fotogramma chiave più vicino viene visualizzato quando non viene riprodotto. Questa modalità non è pertinente per le tracce audio. |
| shuffle    | Le tracce vengono riprodotte in ordine casuale.                                                               |



 

</dd> <dt>

*varfMode* \[ Pollici\]
</dt> <dd>

Valore **System.Boolean** che specifica se la nuova modalità specificata è attiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando la modalità showFrame è attiva, Windows Media Player deve accedere al contenuto della traccia per recuperare il fotogramma video. Usare questa modalità con cautela durante la riproduzione di contenuto non locale.

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

[**IWMPSettings.getMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





