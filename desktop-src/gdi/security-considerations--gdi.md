---
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate a GDI. Questo argomento non fornisce tutte le informazioni necessarie sui problemi di sicurezza. Al contrario, usarlo come punto di partenza e riferimento per questa area di tecnologia.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Considerazioni sulla sicurezza: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c4a7a95fc964e76cdb751cc86d0d0cd3120b5f4cce3e10bc5a83bcbb48a4c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886132"
---
# <a name="security-considerations-gdi"></a>Considerazioni sulla sicurezza: GDI

In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate a GDI. Questo argomento non fornisce tutte le informazioni necessarie sui problemi di sicurezza. Al contrario, usarlo come punto di partenza e riferimento per questa area di tecnologia.

GDI ha in genere pochi problemi di sicurezza perché riguarda la visualizzazione anziché l'input. Tuttavia, ecco alcuni problemi da considerare.

Bitmap, metafile e tipi di carattere sono strutture complesse che potrebbero essere danneggiate. È consigliabile cercare di assicurarsi che questi elementi non siano incorrotta e da un'origine attendibile.

Un'applicazione può specificare il descrittore di sicurezza per alcune DELLE API di stampa e spooling. È necessario fare attenzione quando si imposta il descrittore di sicurezza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Security Central](https://www.microsoft.com/security/)
</dt> <dt>

[Centro per sviluppatori dedicato alla sicurezza](https://technet.microsoft.com/security/)
</dt> <dt>

[Security TechCenter](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



