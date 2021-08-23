---
description: È possibile usare il controllo InkPicture per eseguire il rendering dell'input penna in Microsoft Windows 2000, Windows Server 2003 e nelle edizioni non Tablet PC di Windows XP. Tuttavia, non è possibile usare il controllo per immettere input penna in questi sistemi operativi.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Uso di InkPicture nelle versioni precedenti di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52423e8eb3e4c7f59da7a7caac299428dd8efcdce2192819444bfe91070f10b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091360"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>Uso di InkPicture nelle versioni precedenti di Windows

È possibile usare il [controllo InkPicture](inkpicture-control.md) per eseguire il rendering dell'input penna in Microsoft Windows 2000, Windows Server 2003 e nelle edizioni non Tablet PC di Windows XP. Tuttavia, non è possibile usare il controllo per immettere input penna in questi sistemi operativi.

La proprietà [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) del controllo è impostata su **FALSE** e il tentativo di modifica della proprietà non ha alcun effetto. È possibile assegnare valori ad altre proprietà e modificare l'input penna a livello di codice, ma non è possibile usare il controllo per raccogliere l'input penna.

 

 



