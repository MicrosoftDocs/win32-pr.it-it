---
title: Commenti (Msfeeds.h)
description: Aggiungere commenti ai metafile seguendo la sintassi Extensible Markup Language (XML). I commenti iniziano con \ 0034; -- \ 0034; e terminano con \ 0034;-- \ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Commenti Windows Media Player
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fe5aaf9dde3d804bb91a1e2551636c86aa54ff2bec599bf06100ee2622b592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135784"
---
# <a name="comments-msfeedsh"></a>Commenti (Msfeeds.h)

Aggiungere commenti ai metafile seguendo la sintassi Extensible Markup Language (XML). I commenti iniziano con &lt; "!--" e terminano con "-- &gt; ".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Commenti

I commenti possono essere visualizzati ovunque tranne all'interno del contenuto dell'elemento (tra i tag di apertura e chiusura degli elementi,  < >). Non fanno parte dei dati di tipo carattere del documento e vengono ignorati quando il metafile viene analizzato.

## <a name="examples"></a>Esempio


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





