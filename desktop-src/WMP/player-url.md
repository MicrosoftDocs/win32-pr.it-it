---
title: Player.URL
description: La proprietà URL specifica o recupera il nome dell'elemento multimediale da riprodurre.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player.URL Windows Media Player
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00a6513350ee9c39855aba8168faf9ced788a0686a0fdbe845013dcc521142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572040"
---
# <a name="playerurl"></a>Player.URL

La **proprietà URL** specifica o recupera il nome dell'elemento multimediale da riprodurre.

## <a name="syntax"></a>Sintassi

*lettore* . **URL**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa **di** lettura/scrittura senza alcun valore predefinito.

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata solo su un URL in un'area di sicurezza uguale o meno restrittiva rispetto all'area di sicurezza del programma chiamante o della pagina Web.

Le applicazioni che aprono elementi multimediali da dietro un firewall avranno prestazioni migliori se l'indirizzo viene specificato usando il nome DNS (Domain Name Server) anziché l'indirizzo IP.

Non chiamare questo metodo dal codice del gestore eventi. Chiamata *di Player*. **L'URL** di un gestore eventi può produrre risultati imprevisti.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono creati un elemento di input HTML TEXT e un elemento di input HTML BUTTON. L'elemento TEXT consente all'utente di digitare un percorso per specificare un file multimediale digitale da riprodurre. L'elemento BUTTON viene JScript che apre il file e avvia Windows Media Player. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
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

 

 





