---
title: Commenti (msfeeds. h)
description: Aggiungere commenti ai metafile seguendo la sintassi Extensible Markup Language (XML). I commenti iniziano con \ 0034; --\ 0034; e terminano con \ 0034;--\ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Commenti Media Player Windows
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
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333856"
---
# <a name="comments-msfeedsh"></a>Commenti (msfeeds. h)

Aggiungere commenti ai metafile seguendo la sintassi Extensible Markup Language (XML). I commenti iniziano con " &lt; !--" e terminano con "-- &gt; ".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Commenti

I commenti possono trovarsi ovunque tranne che nel contenuto dell'elemento (tra tag di apertura e chiusura dell'elemento,  < >). Non fanno parte dei dati di tipo carattere del documento e vengono ignorati durante l'analisi del metafile.

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
| Intestazione<br/> | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





