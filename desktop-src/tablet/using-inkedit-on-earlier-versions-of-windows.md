---
description: A causa della mancanza di riconoscitori nelle edizioni non Tablet PC di Microsoft Windows XP, non è possibile utilizzare InkEdit per eseguire il rendering dell'input penna nelle edizioni di Windows XP, Windows 2000, Windows Server 2003 e non Tablet PC e non è possibile utilizzare il controllo per inserire input penna in questi sistemi operativi.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Utilizzo di InkEdit nelle versioni precedenti di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306716"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Utilizzo di InkEdit nelle versioni precedenti di Windows

A causa della mancanza di riconoscitori nelle edizioni non Tablet PC di Microsoft Windows XP, non è possibile utilizzare [InkEdit](inkedit-control.md) per eseguire il rendering dell'input penna nelle edizioni di Windows XP, Windows 2000, windows Server 2003 e non Tablet PC e non è possibile utilizzare il controllo per inserire input penna in questi sistemi operativi.

La proprietà [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del controllo è impostata su **disabled** (**IEM \_ disabled** per C++) e il tentativo di modificare la proprietà non ha alcun effetto. È possibile assegnare valori ad altre proprietà e copiare e incollare l'input penna in altre applicazioni, ma non è possibile utilizzare il controllo per accettare movimenti o raccogliere input penna.

 

 



