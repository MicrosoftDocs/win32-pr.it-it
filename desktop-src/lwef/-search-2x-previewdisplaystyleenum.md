---
title: Enumerazione PreviewDisplayStyle
description: Usato da IResultsViewer PreviewStyle per impostare o determinare lo stile di visualizzazione attualmente in uso.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- Enumerazione PreviewDisplayStyle Funzionalità dell'Windows legacy
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd98a439daeadfd2af6135c1519aea8f981f94394ac68efe142a64037e70a25f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753395"
---
# <a name="previewdisplaystyle-enumeration"></a>Enumerazione PreviewDisplayStyle

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Usato da [**IResultsViewer::P reviewStyle**](-search-2x-iresultsviewer-previewstyle.md) per impostare o determinare lo stile di visualizzazione attualmente in uso.

## <a name="syntax"></a>Sintassi


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**Anteprima automatica**
</dt> <dd>

Indica La visualizzazione automatica.

</dd> <dt>

<span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**Anteprima a destra**
</dt> <dd>

Indica RightPreview.

</dd> <dt>

<span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**
</dt> <dd>

Indica BottomPreview.

</dd> <dt>

<span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**
</dt> <dd>

Indica NoPreview.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView.idl</dt> </dl> |



 

 





