---
title: Impostazioni.invokeURLs
description: La proprietà invokeURLs specifica o recupera un valore che indica se gli eventi URL devono avviare un Web browser.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Impostazioni.invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75de25c5b4a18b6d53423657dc7180fe58cb095f3244800c2c42593d1d450e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002403"
---
# <a name="settingsinvokeurls"></a>Impostazioni.invokeURLs

La **proprietà invokeURLs** specifica o recupera un valore che indica se gli eventi URL devono avviare un Web browser.

## <a name="syntax"></a>Sintassi

player.settings.invokeURLs

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                  |
|-------|----------------------------------------------|
| true  | Valore predefinito. Gli eventi URL devono avviare un browser. |
| false | Gli eventi URL non devono avviare un browser.      |



 

## <a name="remarks"></a>Commenti

I file multimediali possono contenere URL. Quando un URL viene inviato al controllo Windows Media Player, viene passato per primo al gestore dell'evento **ScriptCommand** indipendentemente dal valore in **invokeURLs**. Dopo **la chiusura di ScriptCommand,** Windows Media Player controlla **invokeURLs** per determinare se avviare il browser Internet predefinito con l'URL. È possibile visualizzare in modo selettivo gli URL selezionandoli in **ScriptCommand** e impostando **invokeURLs come** desiderato.

**Windows Media Player 10 Mobile:** questa proprietà accetta o restituisce false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento Player.ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> </dl>

 

 





