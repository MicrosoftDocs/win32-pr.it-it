---
title: Elemento AlbumInfo
description: L'elemento AlbumInfo specifica l'URL per la pagina Web visualizzata da Windows Media Player quando l'utente sceglie di visualizzare altre informazioni su un particolare elemento multimediale.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Finestra elementi AlbumInfo Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328726"
---
# <a name="albuminfo-element"></a>Elemento AlbumInfo

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **AlbumInfo** specifica l'URL per la pagina Web visualizzata da Windows Media Player quando l'utente sceglie di visualizzare altre informazioni su un particolare elemento multimediale.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)
</dt> <dd>

URL per la pagina Web visualizzata da Windows Media Player.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

Quando l'utente fa clic su un pulsante di Windows Media Player per visualizzare informazioni aggiuntive su un particolare elemento multimediale, il lettore Invia la richiesta URL con i parametri allegati usando un separatore di stringa di query punto interrogativo (?). La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità con le versioni precedenti.



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

 

 





