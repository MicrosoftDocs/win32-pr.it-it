---
title: Elemento MOREINFO
description: L'elemento MOREINFO specifica un URL di un sito Web, un indirizzo di posta elettronica o un comando script associato a una visualizzazione, una clip o un banner.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Finestra elementi MOREINFO Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325440"
---
# <a name="moreinfo-element"></a>Elemento MOREINFO

L'elemento **moreinfo** specifica un URL di un sito Web, un indirizzo di posta elettronica o un comando script associato a una visualizzazione, una clip o un banner.

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>Attributi

**Href** (obbligatorio)

URL di un sito Web, un indirizzo di posta elettronica o un comando di script.

**DESTINAZIONE**

Valore che definisce il frame o la finestra in cui il browser aprirà la pagina definita dall'attributo **href** .

Può trattarsi di una stringa contenente il nome di una finestra o di uno dei valori seguenti.



| Valore    | Descrizione                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_vuoto  | Il documento viene caricato in una nuova finestra del browser.                                                                              |
| \_auto   | Il documento viene caricato nello stesso frame del documento corrente contenente il controllo Media Player di Windows.                |
| \_padre | Il documento viene caricato nel frame padre immediato del frame corrente o nel frame corrente se non è presente alcun frame padre. |
| \_In alto    | Il documento viene caricato nella finestra del browser completo, sostituendo tutti gli altri frame o documenti.                                  |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                       |
|-----------------|--------------------------------|
| Elementi padre | **ASX**, **voce**, **banner** |
| Elementi figlio  | nessuno                           |



 

## <a name="remarks"></a>Osservazioni

Questo elemento specifica un URL di un sito Web, un indirizzo di posta elettronica **o un comando di script. L'utente può accedere alla destinazione dell'URL facendo clic sul grafico o sul testo associato all'elemento MOREINFO** . I dettagli dipendono dall'elemento padre dell'elemento **moreinfo** :

-   Se l'elemento **moreinfo** è figlio di un elemento **ASX** , l'utente può accedere all'URL facendo clic sul titolo show.
-   Se l'elemento **moreinfo** è figlio di un elemento **entry** , l'utente può accedere all'URL facendo clic sul titolo della clip.
-   Se l'elemento **moreinfo** è figlio di un elemento **banner** , l'utente può accedere all'URL facendo clic sull'icona del banner.

Se l'attributo **href** specifica un URL di un sito Web, il browser si apre e passa all'URL. Se l'attributo **href** specifica un indirizzo di posta elettronica, viene avviata l'applicazione di posta elettronica dell'utente. Se l'attributo **href** specifica un comando script, il comando script viene eseguito nel browser.

**Nota**

Se l'elemento **moreinfo** viene visualizzato all'interno di un elemento **ASX** o **entry** , quando il cursore del mouse viene posizionato sul titolo della Mostra (per un elemento **ASX** ) o su una clip (per un elemento **entry** ), l'URL definito nell'attributo **href** può essere selezionato e accessibile da Windows Media Player.

L'attributo di **destinazione** consente di definire il frame o la finestra in cui il browser aprirà la pagina definita dall'attributo **href** . I valori per questo attributo seguono la sintassi HTML standard e le definizioni. Nel caso di un controllo incorporato in una pagina Web, se non è stato definito alcun attributo di **destinazione** , l'URL caricherà la finestra del browser corrente e sostituirà la pagina esistente, il che significa che il contenuto smette di essere riprodotto. È pertanto consigliabile specificare sempre un attributo di **destinazione** quando si incorpora il controllo Media Player di Windows in una pagina Web.

Se il metafile viene aperto nel Media Player Windows autonomo, l'attributo di **destinazione** viene ignorato e l'URL viene caricato in una finestra del browser esistente. Se non è presente alcuna finestra del browser attualmente aperta, l'URL viene caricato in una nuova finestra del browser.

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

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





