---
description: impostazioni locali \_ NOUSEROVERRIDE
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312853"
---
# <a name="locale_nouseroverride"></a>impostazioni locali \_ NOUSEROVERRIDE

> [!Caution]  
> Poiché le impostazioni locali \_ NOUSEROVERRIDE Disabilita le preferenze dell'utente, il suo utilizzo è fortemente sconsigliato. Questa costante non garantisce la stabilità dei dati, in quanto [impostazioni locali personalizzate](custom-locales.md), aggiornamenti dei servizi, diverse versioni del sistema operativo e altri scenari possono modificare i dati in modi imprevisti. Per ulteriori informazioni, vedere [utilizzo di dati delle impostazioni locali permanenti](using-persistent-locale-data.md).

 

Nessun override utente. In numerose funzioni, ad esempio, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), questa costante fa in modo che la funzione ignori qualsiasi override utente e usi il valore predefinito di sistema per qualsiasi altra costante specificata nella chiamata di funzione. Le informazioni vengono recuperate dal database delle impostazioni locali, anche se l'identificatore indica le impostazioni locali correnti e l'utente ha modificato alcuni valori usando il pannello di controllo oppure se un'applicazione ha modificato questi valori usando [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Se questa costante non viene specificata, i valori configurati dall'utente dal pannello di controllo o che un'applicazione è stata configurata con [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) hanno la precedenza sulle impostazioni del database per le impostazioni locali predefinite del sistema corrente.

 

 



