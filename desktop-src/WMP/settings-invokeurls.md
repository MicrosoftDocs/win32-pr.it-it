---
title: Settings. invokeURLs
description: La proprietà invokeURLs specifica o recupera un valore che indica se gli eventi URL devono avviare un Web browser.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Impostazioni. invokeURLs Windows Media Player
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
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327383"
---
# <a name="settingsinvokeurls"></a>Settings. invokeURLs

La proprietà **invokeURLs** specifica o recupera un valore che indica se gli eventi URL devono avviare un Web browser.

## <a name="syntax"></a>Sintassi

Player. Settings. invokeURLs

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                  |
|-------|----------------------------------------------|
| true  | Valore predefinito. Gli eventi URL dovrebbero avviare un browser. |
| false | Gli eventi URL non devono avviare un browser.      |



 

## <a name="remarks"></a>Commenti

I file multimediali possono contenere URL. Quando un URL viene inviato al controllo Media Player di Windows, viene passato prima al gestore eventi **ScriptCommand** , indipendentemente dal valore in **invokeURLs**. Dopo la chiusura di **ScriptCommand** , Windows Media Player controlla **invokeURLs** per determinare se avviare il browser Internet predefinito con l'URL. È possibile visualizzare gli URL in modo selettivo e selezionarli in **ScriptCommand** e impostare **invokeURLs** come desiderato.

**Windows Media Player 10 Mobile**: questa proprietà accetta o restituisce false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento Player. ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> </dl>

 

 





