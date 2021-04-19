---
title: Player. URL
description: La proprietà URL specifica o Recupera il nome dell'elemento multimediale da riprodurre.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player. URL Windows Media Player
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
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327061"
---
# <a name="playerurl"></a>Player. URL

La proprietà **URL** specifica o Recupera il nome dell'elemento multimediale da riprodurre.

## <a name="syntax"></a>Sintassi

*Player* . **URL** di

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura senza valore predefinito.

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata solo su un URL in un'area di sicurezza uguale o meno restrittiva rispetto all'area di sicurezza del programma chiamante o della pagina Web.

Le applicazioni che aprono elementi multimediali da dietro un firewall avranno prestazioni migliori se l'indirizzo viene specificato usando il nome del Domain Name Server (DNS) invece dell'indirizzo IP.

Non chiamare questo metodo dal codice del gestore eventi. Chiamata del *lettore*. L' **URL** di un gestore eventi può produrre risultati imprevisti.

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono creati un elemento input di testo HTML e un elemento input BUTTON HTML. L'elemento di testo consente all'utente di digitare un percorso per specificare un file multimediale digitale da riprodurre. L'elemento BUTTON esegue JScript che apre il file e avvia Windows Media Player. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





