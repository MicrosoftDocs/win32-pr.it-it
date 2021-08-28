---
description: A causa della mancanza di riconoscitori nelle edizioni non Tablet PC di Microsoft Windows XP, non è possibile usare InkEdit per eseguire il rendering dell'input penna nelle edizioni Windows 2000, Windows Server 2003 e non Tablet PC di Windows XP e non è possibile usare il controllo per l'input penna in questi sistemi operativi.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Uso di InkEdit nelle versioni precedenti di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa98089a2ede778be09719767f96a1129a1be0d4004828172651e637cd81d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966610"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Uso di InkEdit nelle versioni precedenti di Windows

A causa della mancanza di riconoscitori nelle edizioni non Tablet PC di Microsoft Windows XP, non è possibile usare [InkEdit](inkedit-control.md) per eseguire il rendering dell'input penna nelle edizioni Windows 2000, Windows Server 2003 e non Tablet PC di Windows XP e non è possibile usare il controllo per l'input penna in questi sistemi operativi.

La proprietà [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del controllo è impostata su **Disabled** **(IEM \_ Disabled** per C++) e il tentativo di modifica della proprietà non ha alcun effetto. È possibile assegnare valori ad altre proprietà e copiare e incollare input penna in altre applicazioni, ma non è possibile usare il controllo per accettare movimenti o raccogliere input penna.

 

 



