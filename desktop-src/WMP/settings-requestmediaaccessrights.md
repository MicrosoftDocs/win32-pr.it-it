---
title: metodo Impostazioni.requestMediaAccessRights
description: Il metodo requestMediaAccessRights richiede un livello specificato di accesso alla libreria. | metodo Impostazioni.requestMediaAccessRights
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- Metodo requestMediaAccessRights Windows Media Player
- Metodo requestMediaAccessRights Windows Media Player , Impostazioni classe
- Impostazioni classe Windows Media Player , metodo requestMediaAccessRights
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
ms.openlocfilehash: 1e157e7b4495c8d90964d62a9045eebb202126906f0022e97c4983220e47ac03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569312"
---
# <a name="settingsrequestmediaaccessrights-method"></a>metodo Impostazioni.requestMediaAccessRights

Il **metodo requestMediaAccessRights** richiede un livello specificato di accesso alla libreria.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*accesso* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il livello di diritti di accesso desiderato. Contiene uno dei valori seguenti.



| string | Descrizione                      |
|--------|----------------------------------|
| Nessuno   | Diritti di accesso all'elemento corrente. |
| lettura   | Solo diritti di accesso in lettura.         |
| completi   | Diritti di accesso in lettura/scrittura.        |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano** che indica se i diritti di accesso richiesti sono stati concessi.

## <a name="remarks"></a>Commenti

Una pagina Web deve prima richiedere all'utente l'autorizzazione per leggere o scrivere dati nella libreria. La chiamata di questo metodo richiede all'utente una finestra di dialogo che richiede il livello di autorizzazione specificato. Ciò significa che determinati metodi, proprietà ed eventi non saranno accessibili dal codice se non sono stati concessi i diritti di accesso appropriati. Il livello di diritti di accesso corrente può essere recuperato usando *Impostazioni*. **mediaAccessRights**.

**Windows Media Player 10 Mobile:** questo metodo restituisce sempre **true.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





