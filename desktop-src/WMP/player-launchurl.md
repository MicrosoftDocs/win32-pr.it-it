---
title: Metodo Player.launchURL
description: Il metodo launchURL invia un URL al browser predefinito dell'utente per il rendering. | Metodo Player.launchURL
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- Metodo launchURL Windows Media Player
- Metodo launchURL Windows Media Player , classe Player
- Classe Player Windows Media Player, metodo launchURL
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d22c65a29aaee9c849677dfa42acb5769bf30d2fb7079e305ee79632ef22e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134824"
---
# <a name="playerlaunchurl-method"></a>Metodo Player.launchURL

Il **metodo launchURL** invia un URL al browser predefinito dell'utente per il rendering.

## <a name="syntax"></a>Sintassi


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* \[ Pollici\]
</dt> <dd>

**Valore** stringa che rappresenta l'URL da avviare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo apre solo le pagine Web che usano i protocolli HTTP o HTTPS.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando viene selezionato, visualizza il sito Web Microsoft in una nuova finestra del browser. **L'elemento Player** è stato creato con ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





