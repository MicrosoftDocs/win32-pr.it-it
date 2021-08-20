---
title: Uso di elementi PARAM in una pagina Web visualizzata da Firefox
description: Uso di elementi PARAM in una pagina Web visualizzata da Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows Media Player,PARAM nell'elemento OBJECT
- Windows Media Player a oggetti, elementi PARAM nell'elemento OBJECT
- modello a oggetti,elementi PARAM nell'elemento OBJECT
- Windows Media Player Elementi Mobile,PARAM nell'elemento OBJECT
- Windows Media Player ActiveX controllo,elementi PARAM nell'elemento OBJECT
- Windows Media Player Controllo mobile ActiveX,elementi PARAM nell'elemento OBJECT
- ActiveX controllo, elementi PARAM nell'elemento OBJECT
- incorporamento, pagine Web
- Incorporamento di pagine Web, elementi PARAM nell'elemento OBJECT
- Elementi PARAM nell'elemento OBJECT
- Windows Media Player,Firefox
- Windows Media Player a oggetti, Firefox
- modello a oggetti, Firefox
- Windows Media Player Dispositivi mobili, Firefox
- Windows Media Player ActiveX controllo, Firefox
- Windows Media Player Controllo ActiveX per dispositivi mobili,Firefox
- ActiveX controllo, Firefox
- Elementi Firefox,PARAM nell'elemento OBJECT
- Incorporamento di pagine Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767b9b0d5e4367a17f07f68600ff8e9cac488ca9e4c950165d84677fd7d03956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117306"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Uso di elementi PARAM in una pagina Web visualizzata da Firefox

È possibile usare gli elementi PARAM all'interno di un elemento OBJECT per impostare lo stato iniziale del controllo Player. Ad esempio, gli elementi PARAM nell'esempio seguente specificano che il controllo deve riprodurre automaticamente seattle.wmv.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



La maggior parte degli elementi PARAM può essere interpretata Internet Explorer e da Firefox. Esistono tuttavia alcuni elementi PARAM non supportati dal plug-in Firefox. Per informazioni sugli elementi PARAM supportati dal plug-in Firefox, vedere [Elementi PARAM in un elemento OBJECT.](param-elements-in-an-object-element.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Windows Media Player con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




