---
title: Chiamata di WdS da pagine Web
description: È possibile chiamare Microsoft Windows Desktop Search (WDS) da qualsiasi pagina Web creata o mantenuta usando l'oggetto browser helper (BHO) e Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac2be6be30889e8f759ee3cf7529250a5513ce58
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883705"
---
# <a name="calling-wds-from-web-pages"></a>Chiamata di WdS da pagine Web

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive, usare [Windows ricerca.](../search/-search-3x-wds-overview.md)

È possibile chiamare Microsoft Windows Desktop Search (WDS) da qualsiasi pagina Web creata o mantenuta usando l'oggetto browser helper (BHO) e Windows Internet Explorer. È possibile vedere come funziona nella pagina Web DI MSN. Sopra la casella di ricerca in sono disponibili diversi tipi https://www.msn.com di ricerca: Web, Notizie, Immagini, Desktop, Encarta e Locale. Se si fa clic su Desktop, i parametri di ricerca vengono passati Windows Desktop Search, che cerca nel catalogo e visualizza i risultati nell'interfaccia utente di WdS. Per consentire agli utenti di avviare una ricerca desktop dalle pagine Web, WDSBHO deve essere installato e abilitato nei sistemi, le pagine Web devono essere registrate con WDS come URL consentito ed è necessario creare un collegamento per passare la query enetered utente a WDS.

## <a name="enabling-the-wds-browser-help-object"></a>Abilitazione dell'oggetto Guida del browser WDS

Per impostazione predefinita, QUANDO si installa WDS, l'oggetto VIENE installato e abilitato all'interno di Internet Explorer, ma è possibile verificare facilmente che non sia stato disabilitato o disinstallato. Nel sistema di un utente aprire Internet Explorer , scegliere **Opzioni Internet** dal  **menu** Strumenti, fare clic sulla scheda Programmi e quindi su Gestisci **componenti aggiuntivi**. Nell'elenco dei componenti aggiuntivi cercare la classe dsWebAllowBHO e assicurarsi che sia abilitata. Quando l'impostazione DISA è disabilitata, WDS continuerà a funzionare normalmente. Tuttavia, non sarà possibile eseguire ricerche nel desktop da una pagina Web.

Entrambe le opzioni seguenti per consentire una ricerca desktop eseguiranno la ricerca in locale con l'applicazione di ricerca registrata.

## <a name="registering-web-page-urls"></a>Registrazione degli URL delle pagine Web

Il Registro di sistema include un elenco di URL di dominio "consentiti" da cui è possibile chiamare WdS. Per includere le pagine Web, è necessario elencare gli URL di dominio come REG SZ nel Registro \_ di sistema come indicato di seguito:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **Allowed** \\ *&lt; number &gt;*  =  &lt; domainURL&gt;

Dove **&lt; number &gt;** è numerato in sequenza e **&lt; domainURL &gt;** è l'URL della pagina Web da cui consentire le ricerche wds. Questa stringa URL può includere l'asterisco \* jolly all'inizio o alla fine dell'URL. Ad esempio, se la stringa è ".mydomain.com", è possibile avviare una ricerca \* wds sia https://www.mydomain.com da che da https://mydomain.com .

## <a name="enabling-desktop-search-by-url"></a>Abilitazione di Desktop Search in base all'URL

Un'altra opzione che non richiede l'accesso al Registro di sistema è usare l'URL seguente nelle pagine Web:

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

dove **QUERY** è la stringa con codifica URL in cui l'utente esegue la ricerca, inclusi i [termini della sintassi di query](-search-2x-wds-aqsreference.md) avanzata.

 

 




