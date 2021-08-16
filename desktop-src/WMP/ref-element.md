---
title: Elemento REF
description: L'elemento REF specifica un URL per il contenuto multimediale digitale.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Elemento REF Windows Media Player
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9195eb1fc3ca1f13e64376c0200cbb2e6ec4589e6740a74b1ff7670c0951df25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118333278"
---
# <a name="ref-element"></a>Elemento REF

**L'elemento REF** specifica un URL per il contenuto multimediale digitale.

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>Attributi

**HREF** (obbligatorio)

URL di qualsiasi contenuto multimediale supportato da Windows Media Player.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Elementi padre | **Voce**                                                                        |
| Elementi figlio  | **DURATION,** **ENDMARKER,** **PREVIEWDURATION,** **STARTMARKER,** **STARTTIME** |



 

## <a name="remarks"></a>Commenti

Questo elemento specifica un URL per una parte di contenuto multimediale. L'URL può puntare a qualsiasi tipo di supporto supportato, usando qualsiasi protocollo supportato da Windows Media Player.

I tipi di supporti supportati includono immagini fisse, ad esempio .gif e .jpg e file Flash con estensione swf. Questi tipi di supporti sono utili per includere contenuto pubblicitario all'interno di una playlist. Con i file di immagine e i file Flash riprodotti in un ciclo, è necessario specificare anche la quantità di tempo per visualizzare l'elemento multimediale includendo un **elemento DURATION** all'interno dell'elemento **REF.** Se si vuole che un'immagine continui a essere visualizzata mentre la voce successiva nella playlist  è memorizzata nel buffer, includere un elemento **PARAM** all'interno dell'elemento **ENTRY,** impostarne l'attributo name su ShowWhileBuffering e impostare il relativo attributo **value** su true.

Per fare riferimento al contenuto su un CD o un DVD che lo consente, vengono forniti i protocolli wmpcd e wmpdvd. Ad esempio, se si imposta l'attributo **HREF** su "wmpdvd://f/5/3" verrà riprodotto il capitolo 3 del titolo 5 in un DVD, ma solo se il DVD è stato creato per consentirlo.

Le applicazioni che aprono supporti digitali da dietro un firewall avranno prestazioni migliori quando si aprono gli elementi multimediali se l'indirizzo viene specificato usando il nome DNS (Domain Name Server) anziché l'indirizzo IP.

L'uso più comune di questo elemento è il rollover dell'URL. Se Windows Media Player non è in grado di aprire un elemento multimediale definito in un elemento **REF,** prova l'URL nell'elemento **REF** successivo. Dopo Windows Media Player contenuto multimediale da un URL definito nell'ambito di un elemento **ENTRY,** ignora i tag **REF** successivi all'interno di tale **elemento ENTRY.** Al termine della riproduzione del contenuto, Windows Media Player passa all'elemento **ENTRY** successivo, se presente.

-   **Importante** Dopo Windows Media Player stabilisce una connessione a una parte di contenuto a cui si fa riferimento, ignora tutti gli altri elementi **REF** in tale **ENTRY,** indipendentemente dal fatto che la connessione termini normalmente o in modo anomalo.

Se l'elemento multimediale a cui si fa riferimento è un file di immagine, è necessario usare **l'elemento DURATION** per specificare l'ora di visualizzazione dell'immagine.

**Nota**

Il tentativo di riprodurre file multimediali Flash che includono audio con il primo fotogramma può produrre risultati imprevisti. È consigliabile creare contenuto Flash per riprodurre l'audio non prima del secondo fotogramma.

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
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Protocolli e tipi di file supportati**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





