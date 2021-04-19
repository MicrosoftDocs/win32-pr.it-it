---
title: Elemento PARAM (WMP SDK)
description: L'elemento PARAM definisce un parametro personalizzato associato a una playlist o a un elemento di una playlist.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Finestra elementi PARAM Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332546"
---
# <a name="param-element"></a>PARAM (elemento)

L'elemento **param** definisce un parametro personalizzato associato a una playlist o a un elemento di una playlist.

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a>Parametri

Un parametro può essere associato anche alla visualizzazione anziché a un singolo clip, inserendo questo elemento direttamente dopo il tag **ASX** . A questi elementi viene fatto riferimento con i relativi nomi e un valore di indice che inizia con zero.

> [!Note]  
> Questo elemento **ASX** è disponibile solo per Windows Media Player versione 6,01 e successive. L'installazione standard di Microsoft Internet Explorer 5 include una versione compatibile di Windows Media Player.

 

## <a name="attributes"></a>Attributi

**NOME**

Nome utilizzato per accedere al valore del parametro. Il nome può essere qualsiasi stringa valida. Le stringhe seguenti sono già state definite.



| string                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowShuffle                    | L'attributo **value** specifica se la playlist del metafile consente alla funzionalità Windows Media Player shuffle di riprodurre le voci in ordine casuale. L'attributo **value** può essere impostato su "Yes" o "No". Il valore predefinito è "No".                                                                                                                                                                                                                                                                                                                                                                  |
| CanPause                        | L'attributo **value** specifica se l'utente può sospendere la riproduzione. L'attributo **value** può essere impostato su "Yes" o "No". Il valore predefinito è "Yes".                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CanSeek                         | L'attributo **value** specifica se l'utente può modificare la posizione di riproduzione corrente usando la barra di ricerca, l'avanzamento rapido o l'inversione veloce. L'attributo **value** può essere impostato su "Yes" o "No". Il valore predefinito è "Yes".                                                                                                                                                                                                                                                                                                                                                                    |
| CanSkipBack                     | L'attributo **value** specifica se l'utente può passare all'elemento della playlist precedente **facendo clic su indietro.** L'attributo **value** può essere impostato su "Yes" o "No". Il valore predefinito è "Yes".                                                                                                                                                                                                                                                                                                                                                                                         |
| CanSkipForward                  | L'attributo **value** specifica se l'utente può passare alla voce successiva della playlist facendo clic su **Avanti**. L'attributo **value** può essere impostato su "Yes" o "No". Il valore predefinito è "Yes".                                                                                                                                                                                                                                                                                                                                                                                                  |
| CPRadioID                       | L'attributo **value** specifica l'ID di un feed di radio fornito da un archivio online di tipo 1. Ovvero, l'attributo **value** deve essere uguale al campo RadioID di uno dei feed di radio nel catalogo del negozio online. L'elemento padre è l'elemento **ASX** .                                                                                                                                                                                                                                                                                                                                   |
| Codifica                        | L'attributo **value** è impostato su "UTF-8" per indicare che il metafile è un file con codifica Unicode (UTF-8).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| HtmlFlink                       | L'attributo **value** è una stringa fornita da un archivio online di tipo 1. Windows Media Player passa la stringa al metodo [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , implementato dal plug-in Online Store. Il metodo **GetItemInfo** restituisce l'URL della pagina Web da visualizzare nel riquadro **Now Playing** del lettore. La pagina Web ha accesso a tutti i metodi esposti dall'oggetto **esterno** per il tipo 1. Per un elenco di questi metodi, vedere [oggetto esterno per gli archivi online di tipo 1](external-object-for-type-1-online-stores.md). |
| HTMLView                        | L'attributo **value** specifica un URL che viene visualizzato nel riquadro **ora di riproduzione** del lettore in modalità completa per la durata della playlist o della voce corrente a seconda che l'elemento padre sia l'elemento **ASX** o un elemento **entry** . HTMLView non è supportato per il controllo Media Player di Windows.                                                                                                                                                                                                                                                                               |
| Log:*FieldName* \[ :*spazio dei nomi*\] | L'attributo **value** specifica il valore a cui verrà impostato il campo di log indicato. La parte:*namespace* dell'attributo **Name** è facoltativa.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PreBuffer                       | L'attributo **value** specifica se la voce della playlist successiva inizia a memorizzare il buffer prima della fine della voce corrente, che consente una transizione senza problemi. L'attributo **value** può essere impostato su "true" o "false".                                                                                                                                                                                                                                                                                                                                                                                 |
| ShowWhileBuffering              | L'attributo **value** specifica se un file di immagine a cui fa riferimento l'elemento **entry** corrente continua a essere visualizzato oltre la durata specificata, mentre la voce della playlist successiva viene memorizzata nel buffer. L'attributo **value** può essere impostato su "true" o "false".                                                                                                                                                                                                                                                                                                                                         |



 

**VALUE**

Valore associato a questo parametro. Può essere un valore numerico o stringa.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi           |
|-----------------|--------------------|
| Elementi padre | **ASX**, **voce** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento consente agli utenti di inserire informazioni aggiuntive su ogni clip all'interno dell'elemento **entry** che la contiene. Per recuperare le informazioni sui metadati specificate nella **voce** della playlist, usare il *supporto*. metodo **GetItemInfo** . *Supporti*. il metodo **GetItemInfo** Recupera il valore dell'attributo **value** , dato il nome del parametro. Le versioni precedenti di Windows Media Player recuperare le informazioni sui metadati specificate nella **voce** della playlist, usando il metodo **GetMediaParameter** in base al nome del parametro e un numero di indice per la voce.

Un parametro può essere associato anche alla visualizzazione anziché a un singolo clip, inserendo questo elemento direttamente dopo il tag **ASX** . A questi elementi viene fatto riferimento con i relativi nomi e un valore di indice che inizia con zero.

**Nota**

Questo elemento **ASX** è disponibile solo per Windows Media Player versione 6,01 e successive. L'installazione standard di Microsoft Internet Explorer 5 include una versione compatibile di Windows Media Player.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva, è necessario Windows Media Player 9 serie o versione successiva per gli attributi nome predefiniti, è necessario Windows Media Player 10 o versione successiva per i nomi predefiniti CanPause, CanSeek, CanSkipBack e CanSkipForward<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Registrazione dei dati del flusso**](logging-stream-data.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





