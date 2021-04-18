---
title: Elemento BuyCD
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Finestra elementi BuyCD Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327625"
---
# <a name="buycd-element"></a>Elemento BuyCD

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **BuyCD** specifica gli URL per le pagine Web visualizzate da Windows Media Player quando l'utente sceglie di effettuare un acquisto.

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (obbligatorio)
</dt> <dd>

URL per la pagina Web visualizzata dal negozio online per offrire un CD o un DVD da acquistare in Windows Media Player.

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**
</dt> <dd>

URL per la pagina Web visualizzata nel negozio online per offrire un CD o DVD da acquistare in Windows XP Media Center Edition 2004 Update.

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**
</dt> <dd>

URL per la pagina Web visualizzata dal negozio online per offrire un CD o un DVD da acquistare in una finestra del browser separata. Questo URL viene usato anche da Windows XP Service Pack 2 o versione successiva per la funzionalità **Shop for Music online** .

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

Quando l'utente fa clic su un pulsante o un collegamento in Windows Media Player per acquistare un CD o un DVD, il lettore Invia la richiesta URL a ServiceTask1 con i parametri allegati usando un separatore di stringa di query punto interrogativo (?). La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità con le versioni precedenti.



| Nome         | Valore                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Album*      | Valore dell'attributo **WM/AlbumTitle** per l'elemento multimediale.                                                                                                        |
| *Artista*     | Valore dell'attributo **WM/AlbumArtist** , se esistente, o in caso contrario, il valore dell'attributo **Author** per l'elemento multimediale.                                         |
| *Geoid*      | ID della posizione geografica di Windows. L'ID percorso viene specificato dall'utente nell'area **località** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo. |
| *locale*     | Windows Media Player ID impostazioni locali.                                                                                                                                     |
| *Title*      | Valore dell'attributo **title** per l'elemento multimediale.                                                                                                                |
| *UFID*       | Valore dell'attributo **WM/UniqueFileIdentifier** per l'elemento multimediale.                                                                                              |
| *UserLocale* | ID delle impostazioni locali di Windows. Le impostazioni locali vengono specificate dall'utente nell'area **standard e formati** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.        |
| *version*    | Il numero di versione di Windows Media Player usando il formato seguente: 10.0. x. xxxx o 11.0. x. xxxx.                                                                         |



 

Windows XP Media Center Edition 2004 fornisce agli utenti un'interfaccia utente progettata per essere visualizzata a distanza. È necessario creare pagine Web per il parametro *MediaCenterURL* da visualizzare su schermi di grandi dimensioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





