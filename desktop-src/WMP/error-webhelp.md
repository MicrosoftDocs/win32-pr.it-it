---
title: Metodo Error.webHelp
description: Il metodo webHelp avvia la pagina Windows Media Player Guida Web per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero). | Metodo Error.webHelp
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- Metodo webHelp Windows Media Player
- Metodo webHelp Windows Media Player , classe Error
- Classe Error Windows Media Player metodo , webHelp
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fee647d8f3ddca89ed36c224caab05543715864347700d35ae8e80ee45078cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577875"
---
# <a name="errorwebhelp-method"></a>Metodo Error.webHelp

Il **metodo webHelp** avvia la pagina Windows Media Player Guida Web per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero).

## <a name="syntax"></a>Sintassi


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le pagine della Guida Web contengono sempre le informazioni più recenti e più dettagliate sugli errori Windows Media Player errore. Questo metodo trasferisce automaticamente le altre informazioni necessarie per la Guida Web, ad esempio la versione del sistema operativo in uso.

Per accedere direttamente alle pagine della Guida Web, usare il codice di errore e i collegamenti del centro di supporto seguenti.

-   [Windows Media Player Informazioni sul codice di errore](https://support.microsoft.com/kb/886273)
-   [Windows Media Player Centro soluzioni](https://support.microsoft.com/ph/7763#tab0)

**Windows Media Player 10 Mobile:** Questo metodo ha sempre esito positivo, ma non esegue l'operazione prevista.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che avvia la pagina della Guida Web Windows Media Player Microsoft. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Error**](error-object.md)
</dt> </dl>

 

 





