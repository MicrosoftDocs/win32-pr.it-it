---
title: Chiamata di WDS da pagine Web
description: È possibile chiamare Microsoft Windows Desktop Search (WDS) da qualsiasi pagina Web che si crea o si gestisce utilizzando l'oggetto browser helper (BHO) e Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "104046416"
---
# <a name="calling-wds-from-web-pages"></a>Chiamata di WDS da pagine Web

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

È possibile chiamare Microsoft Windows Desktop Search (WDS) da qualsiasi pagina Web che si crea o si gestisce utilizzando l'oggetto browser helper (BHO) e Windows Internet Explorer. È possibile vedere come funziona nella pagina Web MSN. Sopra la casella di ricerca in https://www.msn.com sono disponibili diversi tipi di ricerca: Web, News, images, desktop, Encarta e local. Se si fa clic su desktop, i parametri di ricerca vengono passati a Windows Desktop Search, che cerca nel catalogo e Visualizza i risultati nell'interfaccia utente di WDS. Per consentire agli utenti di avviare una ricerca desktop dalle pagine Web, WDSBHO deve essere installato e abilitato nei sistemi, le pagine Web devono essere registrate con WDS come URL consentito ed è necessario creare un collegamento per passare la query utente-inserisce a WDS.

## <a name="enabling-the-wds-browser-help-object"></a>Abilitazione dell'oggetto guida del browser WDS

Per impostazione predefinita, la funzionalità BHO viene installata e abilitata in Internet Explorer quando si installa WDS, ma è possibile verificare facilmente che non sia stata disabilitata o disinstallata. Nel sistema di un utente aprire Internet Explorer, scegliere **Opzioni Internet** dal menu **strumenti** , fare clic sulla scheda **programmi** e quindi fare clic su **Gestisci componenti** aggiuntivi. Nell'elenco dei componenti aggiuntivi, cercare la classe dsWebAllowBHO e verificare che sia abilitata. Quando il BHO è disabilitato, WDS continuerà a funzionare normalmente. Tuttavia, non sarà possibile eseguire ricerche sul desktop da una pagina Web.

Entrambe le opzioni seguenti per consentire a una ricerca desktop eseguiranno la ricerca localmente con l'applicazione di ricerca registrata.

## <a name="registering-web-page-urls"></a>Registrazione degli URL della pagina Web

Il registro di sistema include un elenco di URL di dominio "consentiti" da cui è possibile chiamare WDS. Per includere le pagine Web, è necessario elencare gli URL di dominio come REG \_ SZ nel registro di sistema come indicato di seguito:

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **consentito**\\*<number>* = <domainURL>

Dove **<number>** è numerato in sequenza e **<domainURL>** è l'URL della pagina Web da cui si desidera consentire la ricerca di WDS. Questa stringa URL può includere l'asterisco con caratteri jolly \* all'inizio o alla fine dell'URL. Ad esempio, se la stringa è " \* . mydomain.com", è possibile avviare una ricerca WDS sia da https://www.mydomain.com che da https://mydomain.com .

## <a name="enabling-desktop-search-by-url"></a>Abilitazione della ricerca desktop per URL

Un'altra opzione che non richiede l'accesso al registro di sistema consiste nell'usare l'URL seguente nelle pagine Web:

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

dove **query** è la stringa codificata in URL su cui l'utente esegue la ricerca, inclusi eventuali termini della [sintassi di query avanzati](-search-2x-wds-aqsreference.md) .

 

 




