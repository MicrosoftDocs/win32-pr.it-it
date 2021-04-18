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
# <a name="locale_nouseroverride"></a><span data-ttu-id="9b8aa-103">impostazioni locali \_ NOUSEROVERRIDE</span><span class="sxs-lookup"><span data-stu-id="9b8aa-103">LOCALE\_NOUSEROVERRIDE</span></span>

> [!Caution]  
> <span data-ttu-id="9b8aa-104">Poiché le impostazioni locali \_ NOUSEROVERRIDE Disabilita le preferenze dell'utente, il suo utilizzo è fortemente sconsigliato.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-104">Since LOCALE\_NOUSEROVERRIDE disables user preferences, its use is strongly discouraged.</span></span> <span data-ttu-id="9b8aa-105">Questa costante non garantisce la stabilità dei dati, in quanto [impostazioni locali personalizzate](custom-locales.md), aggiornamenti dei servizi, diverse versioni del sistema operativo e altri scenari possono modificare i dati in modi imprevisti.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-105">This constant does not guarantee data stability since [custom locales](custom-locales.md), service updates, different operating system versions, and other scenarios can change data in unexpected ways.</span></span> <span data-ttu-id="9b8aa-106">Per ulteriori informazioni, vedere [utilizzo di dati delle impostazioni locali permanenti](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="9b8aa-106">For more information, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

<span data-ttu-id="9b8aa-107">Nessun override utente.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-107">No user override.</span></span> <span data-ttu-id="9b8aa-108">In numerose funzioni, ad esempio, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), questa costante fa in modo che la funzione ignori qualsiasi override utente e usi il valore predefinito di sistema per qualsiasi altra costante specificata nella chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-108">In several functions, for example, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), this constant causes the function to bypass any user override and use the system default value for any other constant specified in the function call.</span></span> <span data-ttu-id="9b8aa-109">Le informazioni vengono recuperate dal database delle impostazioni locali, anche se l'identificatore indica le impostazioni locali correnti e l'utente ha modificato alcuni valori usando il pannello di controllo oppure se un'applicazione ha modificato questi valori usando [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="9b8aa-109">The information is retrieved from the locale database, even if the identifier indicates the current locale and the user has changed some of the values using the Control Panel, or if an application has changed these values by using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="9b8aa-110">Se questa costante non viene specificata, i valori configurati dall'utente dal pannello di controllo o che un'applicazione è stata configurata con [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) hanno la precedenza sulle impostazioni del database per le impostazioni locali predefinite del sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-110">If this constant is not specified, any values that the user has configured from the Control Panel or that an application has configured using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) take precedence over the database settings for the current system default locale.</span></span>

 

 



