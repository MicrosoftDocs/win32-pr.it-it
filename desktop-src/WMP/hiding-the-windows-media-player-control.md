---
title: Nascondere il controllo Media Player Windows
description: Nascondere il controllo Media Player Windows
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- incorporamento, pagine Web
- Windows Media Player, nascondere il controllo ActiveX
- Modello a oggetti di Windows Media Player, nascondere il controllo ActiveX
- modello a oggetti, che nasconde il controllo ActiveX
- Windows Media Player Mobile, controllo hidingActiveX
- Controllo ActiveX di Windows Media Player, nascondere
- Controllo ActiveX Windows Media Player Mobile, nascondere
- Controllo ActiveX, nascondere
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- Incorporamento di pagine Web, controllo ActiveX nascosto
- nascondere il controllo ActiveX di Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331455"
---
# <a name="hiding-the-windows-media-player-control"></a>Nascondere il controllo Media Player Windows

L'oggetto ActiveX di Windows Media Player viene incorporato in una pagina Web utilizzando l'elemento oggetto. Diversamente dalle versioni precedenti, l'elemento oggetto che definisce Media Player di Windows deve essere inserito nella sezione del corpo di una pagina Web, tra i tag <BODY> e </BODY> . L'inserimento dell'oggetto ActiveX Media Player Windows nella sezione HEAD di una pagina Web per nascondere l'interfaccia utente può produrre risultati imprevisti.

Se si inserisce il controllo ActiveX di Windows Media Player nella sezione del corpo di una pagina Web, verrà visualizzata l'interfaccia utente del controllo. Se non si desidera che venga visualizzata e si desidera creare un'interfaccia utente personalizzata, impostare gli attributi Height e Width dell'elemento OBJECT su zero.

Il controllo può essere reso invisibile anche impostando il *lettore*. proprietà **uiMode** su "invisibile". Questa operazione può essere eseguita usando un tag PARAM, come illustrato nella sezione successiva. In questo caso, lo spazio è riservato per il controllo con altezza e larghezza, ma non viene visualizzato nulla nello spazio riservato fino a quando **uiMode** non viene modificato in un valore diverso da "invisibile".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Media Player di Windows in una pagina Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




