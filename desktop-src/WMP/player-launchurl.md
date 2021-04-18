---
title: Player. launchURL, metodo
description: Il metodo launchURL Invia un URL al browser predefinito dell'utente di cui eseguire il rendering. | Player. launchURL, metodo
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- Metodo launchURL Windows Media Player
- Metodo launchURL Windows Media Player, classe Player
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
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326005"
---
# <a name="playerlaunchurl-method"></a>Player. launchURL, metodo

Il metodo **launchURL** Invia un URL al browser predefinito dell'utente di cui eseguire il rendering.

## <a name="syntax"></a>Sintassi


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* \[ di in\]
</dt> <dd>

Valore **stringa** che rappresenta l'URL da avviare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo apre solo le pagine Web usando i protocolli HTTP o HTTPS.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando selezionato, Visualizza il sito Web Microsoft in una nuova finestra del browser. L'elemento **Player** è stato creato con ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





