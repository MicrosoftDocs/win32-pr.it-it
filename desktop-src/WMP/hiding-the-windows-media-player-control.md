---
title: Nascondere il Windows Media Player controllo
description: Nascondere il Windows Media Player controllo
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Dispositivi mobili, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player ActiveX, pagine Web
- Windows Media Player controllo ActiveX per dispositivi mobili,pagine Web
- ActiveX, pagine Web
- incorporamento, pagine Web
- Windows Media Player,nascondere ActiveX controllo
- Windows Media Player a oggetti, nascondere ActiveX controllo
- modello a oggetti, nascondere ActiveX controllo
- Windows Media Player Mobile, nascondere il controlloActiveX
- Windows Media Player ActiveX, nascondere
- Windows Media Player Controllo ActiveX mobile, nascondere
- ActiveX, nascondere
- Windows Media Player ActiveX, pagine Web
- Windows Media Player controllo ActiveX per dispositivi mobili,pagine Web
- ActiveX, pagine Web
- Incorporamento di pagine Web, nascondere ActiveX controllo
- nascondere Windows Media Player ActiveX controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb0b29bbbc1b2eb978c5bd9f29a58aa02bf629d5c6befe9f1dc68bbc92d280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339182"
---
# <a name="hiding-the-windows-media-player-control"></a>Nascondere il Windows Media Player controllo

L Windows Media Player ActiveX o object viene incorporato in una pagina Web usando l'elemento OBJECT. A differenza delle versioni precedenti, l'elemento OBJECT che Windows Media Player deve essere inserito nella sezione BODY di una pagina Web, tra <BODY> e </BODY> Tag. L'inserimento Windows Media Player ActiveX'oggetto nella sezione HEAD di una pagina Web per nascondere l'interfaccia utente può produrre risultati imprevisti.

Se si Windows Media Player ActiveX controllo nella sezione BODY di una pagina Web, verrà visualizzata l'interfaccia utente del controllo. Se non si vuole che sia visualizzata e si vuole creare un'interfaccia utente personalizzata, impostare gli attributi di altezza e larghezza dell'elemento OBJECT su zero.

Il controllo può anche essere reso invisibile impostando l'oggetto *Player.* **Proprietà uiMode** su "invisibile". Questa operazione può essere eseguita usando un tag PARAM, come illustrato nella sezione successiva. In questo caso, lo spazio è riservato per il controllo usando altezza e larghezza, ma non viene visualizzato nulla nello spazio riservato fino a quando **uiMode** non viene modificato in un valore diverso da "invisibile".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo del Windows Media Player in una pagina Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




