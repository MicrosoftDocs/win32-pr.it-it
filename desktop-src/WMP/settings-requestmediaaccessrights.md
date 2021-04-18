---
title: Settings. requestMediaAccessRights, metodo
description: Il metodo requestMediaAccessRights richiede un livello specificato di accesso alla libreria. | Settings. requestMediaAccessRights, metodo
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- Metodo requestMediaAccessRights Windows Media Player
- Metodo requestMediaAccessRights Media Player Windows, classe Settings
- Classe Settings Media Player Windows, metodo requestMediaAccessRights
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327370"
---
# <a name="settingsrequestmediaaccessrights-method"></a>Settings. requestMediaAccessRights, metodo

Il metodo **requestMediaAccessRights** richiede un livello specificato di accesso alla libreria.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*accesso* \[ a in\]
</dt> <dd>

**Stringa** che specifica il livello di diritti di accesso desiderato. Contiene uno dei valori seguenti.



| string | Descrizione                      |
|--------|----------------------------------|
| Nessuno   | Solo diritti di accesso agli elementi correnti. |
| lettura   | Solo diritti di accesso in lettura.         |
| completi   | Diritti di accesso in lettura/scrittura.        |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **booleano** che indica se sono stati concessi i diritti di accesso richiesti.

## <a name="remarks"></a>Commenti

Una pagina Web deve prima richiedere all'utente l'autorizzazione per la lettura o la scrittura di dati nella libreria. La chiamata di questo metodo richiede all'utente una finestra di dialogo che richiede il livello di autorizzazione specificato. Ciò significa che determinati metodi, proprietà ed eventi saranno inaccessibili dal codice se non sono stati concessi i diritti di accesso appropriati. Il livello dei diritti di accesso corrente può essere recuperato usando *le impostazioni*. **mediaAccessRights**.

**Windows Media Player 10 Mobile**: questo metodo restituisce sempre **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





