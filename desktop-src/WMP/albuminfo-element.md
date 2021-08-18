---
title: Elemento AlbumInfo
description: L'elemento AlbumInfo specifica l'URL per la pagina Web Windows Media Player quando l'utente sceglie di visualizzare altre informazioni su un particolare elemento multimediale.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Elemento AlbumInfo Windows Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a5f8fab7da8f61ce6ee5451ebcef4dc33517aae2396f0817fac19222713db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055379"
---
# <a name="albuminfo-element"></a>Elemento AlbumInfo

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

**L'elemento AlbumInfo** specifica l'URL per la pagina Web Windows Media Player visualizzata quando l'utente sceglie di visualizzare altre informazioni su un particolare elemento multimediale.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)
</dt> <dd>

URL per la pagina Web Windows Media Player visualizzata.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

Quando l'utente fa clic su un pulsante in Windows Media Player per visualizzare informazioni aggiuntive su un particolare elemento multimediale, il lettore invia la richiesta URL con i parametri associati usando un punto interrogativo (?) separatore della stringa di query. La tabella seguente contiene informazioni dettagliate sui parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità legacy.



| Nome         | Valore                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Album*      | Valore **dell'attributo WM/AlbumTitle** per l'elemento multimediale.                                                                                                        |
| *Artista*     | Valore **dell'attributo WM/AlbumArtist,** se presente, oppure valore dell'attributo **Author** per l'elemento multimediale.                                         |
| *Geoid*      | Windows'ID della posizione geografica. L'ID località viene specificato dall'utente nell'area **Località** delle impostazioni Opzioni internazionali e della lingua Pannello di controllo. |
| *locale*     | Windows Media Player ID delle impostazioni locali.                                                                                                                                     |
| *Title*      | Valore **dell'attributo Title** per l'elemento multimediale.                                                                                                                |
| *UFID*       | Valore **dell'attributo WM/UniqueFileIdentifier** per l'elemento multimediale.                                                                                              |
| *userlocale* | Windows ID delle impostazioni locali. Le impostazioni locali vengono specificate dall'utente nell'area **Standard** e formati delle impostazioni Opzioni internazionali e della lingua Pannello di controllo.        |
| *version*    | Windows Media Player numero di versione usando il formato seguente: 10.0.x.xxxx o 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per uno store online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





