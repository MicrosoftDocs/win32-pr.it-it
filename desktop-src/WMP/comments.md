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
# <a name="comments-msfeedsh"></a><span data-ttu-id="112b1-105">Commenti (msfeeds. h)</span><span class="sxs-lookup"><span data-stu-id="112b1-105">Comments (Msfeeds.h)</span></span>

<span data-ttu-id="112b1-106">Aggiungere commenti ai metafile seguendo la sintassi Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="112b1-106">Add comments to metafiles by following Extensible Markup Language (XML) syntax.</span></span> <span data-ttu-id="112b1-107">I commenti iniziano con " &lt; !--" e terminano con "-- &gt; ".</span><span class="sxs-lookup"><span data-stu-id="112b1-107">Comments begin with "&lt;!--" and end with "--&gt;".</span></span>

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a><span data-ttu-id="112b1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="112b1-108">Remarks</span></span>

<span data-ttu-id="112b1-109">I commenti possono trovarsi ovunque tranne che nel contenuto dell'elemento (tra tag di apertura e chiusura dell'elemento,  < >).</span><span class="sxs-lookup"><span data-stu-id="112b1-109">Comments can appear anywhere except within element content (between element open and close tags, < >).</span></span> <span data-ttu-id="112b1-110">Non fanno parte dei dati di tipo carattere del documento e vengono ignorati durante l'analisi del metafile.</span><span class="sxs-lookup"><span data-stu-id="112b1-110">They are not part of the document's character data and are ignored when the metafile is parsed.</span></span>

## <a name="examples"></a><span data-ttu-id="112b1-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="112b1-111">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="112b1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="112b1-112">Requirements</span></span>



| <span data-ttu-id="112b1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="112b1-113">Requirement</span></span> | <span data-ttu-id="112b1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="112b1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="112b1-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="112b1-115">Header</span></span><br/> | <dl> <span data-ttu-id="112b1-116"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="112b1-116"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="112b1-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="112b1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112b1-118">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="112b1-118">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





