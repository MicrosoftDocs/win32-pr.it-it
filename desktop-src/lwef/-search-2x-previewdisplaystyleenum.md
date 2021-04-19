---
title: Enumerazione PreviewDisplayStyle
description: Usato da IResultsViewer PreviewStyle per impostare o determinare lo stile di visualizzazione attualmente in uso.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione PreviewDisplayStyle
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
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332808"
---
# <a name="previewdisplaystyle-enumeration"></a>Enumerazione PreviewDisplayStyle

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Usato da [**IResultsViewer::P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) per impostare o determinare lo stile di visualizzazione attualmente in uso.

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

<span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**AutoPreview**
</dt> <dd>

Indica l'anteprima automatica.

</dd> <dt>

<span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**
</dt> <dd>

Indica RightPreview.

</dd> <dt>

<span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**
</dt> <dd>

Indica BottomPreview.

</dd> <dt>

<span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Nopreview**
</dt> <dd>

Indica nopreview.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





