---
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate a GDI. Questo argomento non fornisce tutte le informazioni necessarie per i problemi di sicurezza. È invece possibile utilizzarlo come punto di partenza e riferimento per questa area tecnologica.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Considerazioni sulla sicurezza: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967947"
---
# <a name="security-considerations-gdi"></a>Considerazioni sulla sicurezza: GDI

In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate a GDI. Questo argomento non fornisce tutte le informazioni necessarie per i problemi di sicurezza. È invece possibile utilizzarlo come punto di partenza e riferimento per questa area tecnologica.

In genere, GDI presenta pochi problemi di sicurezza perché gestisce la visualizzazione anziché l'input. Tuttavia, di seguito sono riportate alcune problematiche da prendere in considerazione.

Bitmap, metafile e tipi di carattere sono strutture complesse che potrebbero essere danneggiate. È consigliabile provare a verificare che questi elementi non siano danneggiati e da un'origine attendibile.

Un'applicazione può specificare il descrittore di sicurezza per alcune delle API di stampa e di spooling. È necessario prestare attenzione quando si imposta il descrittore di sicurezza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Security Central](https://www.microsoft.com/security/)
</dt> <dt>

[Centro per sviluppatori dedicato alla sicurezza](https://technet.microsoft.com/security/)
</dt> <dt>

[Security TechCenter](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



