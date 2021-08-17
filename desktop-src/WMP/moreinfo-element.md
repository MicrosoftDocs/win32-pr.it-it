---
title: Elemento MOREINFO
description: L'elemento MOREINFO specifica un URL per un sito Web, un indirizzo di posta elettronica o un comando script associato a uno show, clip o banner.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Elemento MOREINFO Windows Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 925783b6bd48fbc8b944d7b8fd2a2b94a9954c7036114145b99b015b90cbb6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134954"
---
# <a name="moreinfo-element"></a>Elemento MOREINFO

**L'elemento MOREINFO** specifica un URL per un sito Web, un indirizzo di posta elettronica o un comando script associato a uno show, clip o banner.

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>Attributi

**HREF** (obbligatorio)

URL di un sito Web, di un indirizzo di posta elettronica o di un comando script.

**bersaglio**

Valore che definisce il frame o la finestra in cui il browser aprirà la pagina definita **dall'attributo HREF.**

Può trattarsi di una stringa contenente un nome di finestra o di uno dei valori seguenti.



| Valore    | Descrizione                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_Vuoto  | Il documento viene caricato in una nuova finestra del browser.                                                                              |
| \_stesso   | Il documento viene caricato nello stesso frame del documento corrente contenente il Windows Media Player controllo .                |
| \_genitore | Il documento viene caricato nel frame padre diretto del frame corrente o nel frame corrente se non è presente alcun frame padre. |
| \_In alto    | Il documento viene caricato nell'intera finestra del browser, sostituendo tutti gli altri frame o documenti.                                  |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                       |
|-----------------|--------------------------------|
| Elementi padre | **ASX,** **VOCE,** **BANNER** |
| Elementi figlio  | nessuno                           |



 

## <a name="remarks"></a>Osservazioni

Questo elemento specifica un URL per un sito Web, un indirizzo di posta elettronica **o un comando script. L'utente può accedere alla destinazione dell'URL facendo clic sull'elemento grafico o sul testo associato all'elemento MOREINFO.** I dettagli dipendono dall'elemento padre **dell'elemento MOREINFO:**

-   Se **l'elemento MOREINFO** è l'elemento figlio di un **elemento ASX,** l'utente può accedere all'URL facendo clic sul titolo di visualizzazione.
-   Se **l'elemento MOREINFO** è l'elemento figlio di un **elemento ENTRY,** l'utente può accedere all'URL facendo clic sul titolo del clip.
-   Se **l'elemento MOREINFO** è figlio di un **elemento BANNER,** l'utente può accedere all'URL facendo clic sull'icona del banner.

Se **l'attributo HREF** specifica un URL per un sito Web, il browser si apre e passa all'URL. Se **l'attributo HREF** specifica un indirizzo di posta elettronica, viene avviata l'applicazione di posta elettronica dell'utente. Se **l'attributo HREF** specifica un comando script, il comando script viene eseguito nel browser.

**Nota**

Se l'elemento **MOREINFO** viene visualizzato all'interno di un elemento **ASX** o **ENTRY,** quando il cursore del mouse viene posizionato sul titolo della visualizzazione (per un elemento **ASX)** o di un clip (per un elemento **ENTRY),** l'URL definito nell'attributo **HREF** può essere selezionato e accessibile da Windows Media Player.

**L'attributo TARGET** definisce il frame o la finestra in cui il browser aprirà la pagina definita dall'attributo **HREF.** I valori per questo attributo seguono la sintassi e le definizioni HTML standard. Nel caso di un controllo incorporato in una pagina Web, se non è definito alcun attributo **TARGET,** l'URL carica la finestra del browser corrente e sostituisce la pagina esistente, il che significa che la riproduzione del contenuto viene interrotta. È pertanto consigliabile specificare sempre un attributo **TARGET** quando si incorpora il controllo Windows Media Player in una pagina Web.

Se il metafile viene aperto nel Windows Media Player autonomo, l'attributo **TARGET** viene ignorato e l'URL viene caricato in una finestra del browser esistente. Se non è attualmente aperta alcuna finestra del browser, l'URL viene caricato in una nuova finestra del browser.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





