---
title: IWMPSettings metodo semodalità
description: Il metodo semode imposta la modalità ciclo o shuffle su attivo o inattivo.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- Metodo di Media Player di Windows
- Metodo di Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, metodo semode
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
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324520"
---
# <a name="iwmpsettingssetmode-method"></a>Metodo IWMPSettings:: toMode

Il metodo **semode** imposta la modalità ciclo o shuffle su attivo o inattivo.

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

*bstrMode* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome della modalità da modificare, contenente uno dei valori seguenti.



| Valore      | Descrizione                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| riavvolgimento rapido | Le tracce vengono riavviate dall'inizio dopo la riproduzione fino alla fine.                                |
| loop       | La sequenza di tracce si ripete.                                                           |
| showFrame  | Il fotogramma chiave più vicino viene visualizzato in caso di mancata riproduzione. Questa modalità non è pertinente per le tracce audio. |
| shuffle    | Le tracce vengono riprodotte in ordine casuale.                                                               |



 

</dd> <dt>

*varfMode* \[ in\]
</dt> <dd>

Valore **System. Boolean** che specifica se la nuova modalità specificata è attiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando la modalità showFrame è attiva, Windows Media Player deve accedere al contenuto della traccia per recuperare il frame video. Usare questa modalità con cautela per la riproduzione di contenuto non locale.

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

[**IWMPSettings. getMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





