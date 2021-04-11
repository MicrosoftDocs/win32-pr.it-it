---
title: Uso di elementi PARAM in una pagina Web visualizzata da Firefox
description: Uso di elementi PARAM in una pagina Web visualizzata da Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Media Player di Windows, elementi PARAM nell'elemento OBJECT
- Modello a oggetti di Windows Media Player, elementi PARAM nell'elemento OBJECT
- modello a oggetti, elementi PARAM nell'elemento OBJECT
- Windows Media Player Mobile, elementi PARAM nell'elemento oggetto
- Controllo ActiveX Windows Media Player, elementi PARAM nell'elemento OBJECT
- Controllo ActiveX Windows Media Player Mobile, elementi PARAM nell'elemento oggetto
- Controllo ActiveX, elementi PARAM nell'elemento OBJECT
- incorporamento, pagine Web
- Incorporamento di pagine Web, elementi PARAM nell'elemento OBJECT
- Elementi PARAM nell'elemento OBJECT
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Windows Media Player Mobile, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX Windows Media Player Mobile, Firefox
- Controllo ActiveX, Firefox
- Firefox, elementi PARAM nell'elemento OBJECT
- Incorporamento di pagine Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332868"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Uso di elementi PARAM in una pagina Web visualizzata da Firefox

È possibile usare gli elementi PARAM all'interno di un elemento oggetto per impostare lo stato iniziale del controllo Player. Ad esempio, gli elementi PARAM nell'esempio seguente specificano che il controllo deve riprodurre automaticamente Seattle. wmv.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



La maggior parte degli elementi PARAM può essere interpretata da Internet Explorer e da Firefox. Tuttavia, esistono alcuni elementi PARAM che il plug-in di Firefox non supporta. Per informazioni sugli elementi PARAM supportati dal plug-in di Firefox, vedere [elementi param in un elemento Object](param-elements-in-an-object-element.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Media Player Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




