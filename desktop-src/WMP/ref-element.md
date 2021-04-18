---
title: REF-elemento
description: L'elemento REF specifica un URL per il contenuto multimediale digitale.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Media Player di Windows per elementi REF
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327288"
---
# <a name="ref-element"></a>REF-elemento

L'elemento **ref** specifica un URL per il contenuto multimediale digitale.

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>Attributi

**Href** (obbligatorio)

URL di qualsiasi contenuto multimediale supportato da Windows Media Player.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Elementi padre | **VOCE**                                                                        |
| Elementi figlio  | **Duration**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **StartTime** |



 

## <a name="remarks"></a>Commenti

Questo elemento specifica un URL per una porzione di contenuto multimediale. L'URL può puntare a qualsiasi tipo di supporto supportato, usando qualsiasi protocollo supportato da Windows Media Player.

I tipi di supporto supportati includono immagini ancora come le immagini. gif e. jpg e i file Flash con estensione di file SWF. Questi tipi di supporti sono utili per includere contenuti pubblicitari all'interno di una playlist. Con i file di immagine e i file Flash che rientrano in un ciclo, è inoltre necessario specificare la quantità di tempo per la visualizzazione dell'elemento multimediale includendo un elemento **Duration** all'interno dell'elemento **ref** . Se si vuole che un'immagine continui a essere visualizzata mentre la voce successiva nella playlist è memorizzata nel buffer, includere un elemento **param** nell'elemento **entry** , impostare il relativo attributo **Name** su ShowWhileBuffering e impostare il relativo attributo **value** su true.

Per fare riferimento al contenuto di un CD o di un DVD che lo consente, vengono forniti i protocolli wmpcd e wmpdvd. Se ad esempio si imposta l'attributo **href** su "wmpdvd://f/5/3", il capitolo 3 del titolo 5 verrà riprodotto in un DVD, ma solo se il DVD è stato creato per consentirlo.

Le applicazioni che aprono supporti digitali da dietro un firewall avranno prestazioni migliori quando si aprono gli elementi multimediali se l'indirizzo viene specificato usando il nome del Domain Name Server (DNS) invece dell'indirizzo IP.

L'uso più comune di questo elemento è per il rollover degli URL. Se Windows Media Player non è in grado di aprire un elemento multimediale definito in un elemento **ref** , tenta l'URL nell'elemento **ref** successivo. Quando Windows Media Player apre contenuto multimediale da un URL definito nell'ambito di un elemento **entry** , ignora i tag **ref** successivi all'interno dell'elemento **entry** . Una volta completata la riproduzione del contenuto, Windows Media Player si sposta sull'elemento **entry** successivo, se disponibile.

-   **Importante** Una volta che Windows Media Player stabilisce una connessione a una parte di contenuto a cui si fa riferimento, ignora tutti gli altri elementi **ref** in tale **voce**, indipendentemente dal fatto che la connessione termini normalmente o in modo anomalo.

Se l'elemento multimediale a cui si fa riferimento è un file di immagine, è necessario usare l'elemento **Duration** per specificare l'ora di visualizzazione per l'immagine.

**Nota**

Il tentativo di riprodurre supporti flash che includono suoni con il primo frame può produrre risultati imprevisti. È necessario creare il contenuto Flash per riprodurre un suono che inizia senza precedenti rispetto al secondo frame.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Protocolli e tipi di file supportati**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





