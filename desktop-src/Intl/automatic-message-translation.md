---
description: Le applicazioni che usano le funzioni API Unicode e set di caratteri usano in genere la stessa classe di finestra. Il sistema operativo converte in modo trasparente i messaggi tra finestre di classi diverse.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Conversione automatica dei messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5de492e9f24da9e8a9d298e68af2c6d4956f23ad29212c0673e7484dd45d3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119297291"
---
# <a name="automatic-message-translation"></a>Conversione automatica dei messaggi

Le applicazioni che usano le funzioni API Unicode e set di caratteri usano in genere la stessa classe di finestra. Il sistema operativo converte in modo trasparente i messaggi tra finestre di classi diverse.

Viene implementata una funzione finestra per ricevere messaggi in formato Unicode Windows tabella codici. La funzione window può inviare messaggi o chiamare funzioni di entrambi i tipi.

I messaggi seguenti hanno argomenti di testo e sono soggetti alla traduzione automatica del testo. Per informazioni sulla conversione automatica, vedere [Creazione di sottoclassi e Conversione automatica dei messaggi.](subclassing-and-automatic-message-translation.md)

<dl>

[CB \_ ADDSTRING](../controls/cb-addstring.md)  
[CB \_ DIR](../controls/cb-dir.md)  
[CB \_ FINDSTRING](../controls/cb-findstring.md)  
[CB \_ GETLBTEXT](../controls/cb-getlbtext.md)  
[CB \_ INSERTSTRING](../controls/cb-insertstring.md)  
[CB \_ SELECTSTRING](../controls/cb-selectstring.md)  
[EM \_ GETLINE](../controls/em-getline.md)  
[EM \_ REPLACESEL](../controls/em-replacesel.md)  
[EM \_ SETPASSWORDCHAR](../controls/em-setpasswordchar.md)  
[LB \_ ADDFILE](../controls/lb-addfile.md)  
[LB \_ ADDSTRING](../controls/lb-addstring.md)  
[LB \_ DIR](../controls/lb-dir.md)  
[LB \_ FINDSTRING](../controls/lb-findstring.md)  
[LB \_ GETTEXT](../controls/lb-gettext.md)  
[LB \_ INSERTSTRING](../controls/lb-insertstring.md)  
[LB \_ SELECTSTRING](../controls/lb-selectstring.md)  
[WM \_ ASKCBFORMATNAME](../dataxchg/wm-askcbformatname.md)  
[WM \_ CHAR](../inputdev/wm-char.md)  
[WM \_ CHARTOITEM](../controls/wm-chartoitem.md)  
[WM \_ CREATE](../winmsg/wm-create.md)  
[WM \_ DEADCHAR](../inputdev/wm-deadchar.md)  
[WM \_ DEVMODECHANGE](../gdi/wm-devmodechange.md)  
[WM \_ GETTEXT](../winmsg/wm-gettext.md)  
[WM \_ MDICREATE](../winmsg/wm-mdicreate.md)  
[WM \_ MENUCHAR](../menurc/wm-menuchar.md)  
[WM \_ NCCREATE](../winmsg/wm-nccreate.md)  
[WM \_ SETTEXT](../winmsg/wm-settext.md)  
[WM \_ SYSCHAR](../menurc/wm-syschar.md)  
[WM \_ SYSDEADCHAR](../inputdev/wm-sysdeadchar.md)  
[WM \_ WININICHANGE](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
