---
title: Errore. Webhelp (metodo)
description: Il metodo WebHelp avvia la pagina della Guida Web di Windows Media Player per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero). | Errore. Webhelp (metodo)
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- Metodo WebHelp Media Player Windows
- Metodo WebHelp Media Player Windows, classe Error
- Classe Error Media Player Windows, metodo Webhelp
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
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331587"
---
# <a name="errorwebhelp-method"></a>Errore. Webhelp (metodo)

Il metodo **WebHelp** avvia la pagina della Guida Web di Windows Media Player per visualizzare altre informazioni sul primo errore nella coda degli errori (indice zero).

## <a name="syntax"></a>Sintassi


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le pagine della Guida Web contengono sempre le informazioni più recenti e dettagliate sugli errori di Windows Media Player. Questo metodo trasferisce automaticamente le altre informazioni richieste dalla guida Web, ad esempio la versione del sistema operativo in uso.

Per accedere direttamente alle pagine della Guida Web, usare i collegamenti seguenti per il codice di errore e il supporto tecnico.

-   [Informazioni sul codice di errore di Windows Media Player](https://support.microsoft.com/kb/886273)
-   [Centro soluzioni Windows Media Player](https://support.microsoft.com/ph/7763#tab0)

**Windows Media Player 10 Mobile:** Questo metodo ha sempre esito positivo, ma non esegue l'operazione desiderata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento BUTTON HTML che avvia la pagina della Guida Web di Microsoft Windows Media Player. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Error**](error-object.md)
</dt> </dl>

 

 





