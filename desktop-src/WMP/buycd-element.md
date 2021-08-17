---
title: Elemento BuyCD
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. | Elemento BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Elemento BuyCD Windows Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0b2af0f12b06c7d5701db3fcc073d7b7c330e8798408206b64a8b9811f27d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135844"
---
# <a name="buycd-element"></a>Elemento BuyCD

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'elemento BuyCD** specifica gli URL per le pagine Web Windows Media Player quando l'utente sceglie di effettuare un acquisto.

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

URL della pagina Web visualizzata dal negozio online per offrire un CD o un DVD per l'acquisto in Windows Media Player.

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**
</dt> <dd>

URL per la pagina Web visualizzata dal negozio online per offrire un CD o un DVD da acquistare Windows XP Media Center Edition 2004 Update.

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**
</dt> <dd>

URL della pagina Web visualizzata dal negozio online per offrire un CD o un DVD per l'acquisto in una finestra del browser separata. Questo URL viene usato anche da Windows XP Service Pack 2 o versione successiva per la funzionalità **online Acquista** musica.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

Quando l'utente fa clic su un pulsante o un collegamento in Windows Media Player per acquistare un CD o DVD, il lettore invia la richiesta URL a ServiceTask1 con i parametri associati usando un separatore di stringa di query punto interrogativo (?). Nella tabella seguente sono riportati i dettagli dei parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità legacy.



| Nome         | Valore                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Album*      | Valore **dell'attributo WM/AlbumTitle** per l'elemento multimediale.                                                                                                        |
| *Artista*     | Valore **dell'attributo WM/AlbumArtist,** se presente, oppure valore dell'attributo **Author** per l'elemento multimediale.                                         |
| *Geoid*      | Windows ID località geografica. L'ID località viene specificato dall'utente nell'area **Località** delle impostazioni opzioni internazionali e della lingua in Pannello di controllo. |
| *locale*     | Windows Media Player ID impostazioni locali.                                                                                                                                     |
| *Title*      | Valore **dell'attributo Title** per l'elemento multimediale.                                                                                                                |
| *UFID*       | Valore **dell'attributo WM/UniqueFileIdentifier** per l'elemento multimediale.                                                                                              |
| *userlocale* | Windows ID impostazioni locali. Le impostazioni locali vengono specificate dall'utente nell'area **Standard** e formati delle impostazioni opzioni internazionali e della lingua Pannello di controllo.        |
| *version*    | Windows Media Player numero di versione usando il formato seguente: 10.0.x.xxxx o 11.0.x.xxxx.                                                                         |



 

Windows XP Media Center Edition 2004 offre agli utenti un'interfaccia utente progettata per essere visualizzata a distanza. È consigliabile creare pagine Web per il *parametro MediaCenterURL* da visualizzare su schermi di grandi dimensioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





