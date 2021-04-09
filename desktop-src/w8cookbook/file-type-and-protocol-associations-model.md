---
title: Tipo di file e modello di associazioni URI
description: Tipo di file e modello di associazioni URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047498"
---
# <a name="file-type-and-uri-associations-model"></a>Tipo di file e modello di associazioni URI

## <a name="platforms"></a>Piattaforme

 **Client** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>Descrizione

Il tipo di file e il modello di associazione URI sono stati modificati in Windows 8. Le app non sono più in grado di impostarsi a livello di codice come gestore predefinito per un tipo di file o un URI. Al contrario, ora l'utente controlla sempre il tipo di gestore predefinito per un tipo di file o uno schema URI.

## <a name="manifestation"></a>Manifestazione

Il modo in cui questa modifica viene presentata all'utente dipende dal modo in cui viene progettata l'app, ad esempio:

-   Molte app verificano se sono l'impostazione predefinita ogni volta che vengono eseguite e, in caso contrario, richiedono all'utente di impostarle come predefinite. Tuttavia, poiché le app non possono più eseguire query in modo accurato per determinare quale app è il gestore predefinito per un tipo di file o uno schema URI, nessuna di queste operazioni funziona.
-   Molte app hanno una finestra di dialogo o un menu incorporato o nel programma di installazione che specifica i tipi di file per i quali l'app deve fungere da impostazione predefinita. Tuttavia, poiché le app non possono più essere impostate a livello di codice come gestore predefinito per un tipo di file o uno schema URI, questo non funziona più.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Sono disponibili diverse operazioni che gli utenti possono eseguire per gestire le modifiche:

-   Agli utenti viene richiesto di scegliere un'app predefinita per gestire i tipi di file, gli schemi URI o entrambi quando non ne è stato specificato uno.
-   Agli utenti viene offerta la possibilità di modificare il gestore predefinito dopo l'installazione di nuove app in grado di gestire un tipo di file o uno schema URI
-   Il pannello di controllo programmi predefiniti consente agli utenti di impostare le impostazioni predefinite per un'app o per un tipo di file, uno schema URI o entrambi. le app possono essere collegate al pannello di controllo
-   Le impostazioni predefinite possono essere modificate da Esplora risorse

## <a name="solution"></a>Soluzione

In seguito a queste modifiche, viene fornita questa guida sull'API:

-   La funzionalità di alcune chiamate al metodo all'interno dell'API [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) è cambiata e non deve più essere utilizzata.

    -   **Non chiamare** [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) per determinare se un'app è l'impostazione predefinita
    -   **Non** chiamare [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) per determinare quale applicazione (se presente) è l'impostazione predefinita corrente
    -   **Non chiamare** [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) per impostare l'app predefinita

-   Il materiale sussidiario in futuro è:

    -   **Non eseguire una query per** vedere quale app è il gestore predefinito per i tipi di file o gli schemi URI

    -   **Non** tentare di monitorare le modifiche nel gestore predefinito per i tipi di file o gli schemi URI

    -   **Non** tentare di impostare un'app come gestore predefinito per i tipi di file o gli schemi URI

    -   **Non** tentare di gestire i valori predefiniti per i tipi di file o gli schemi URI dall'interno di un'app

    -   **Eseguire** l'integrazione con il pannello di controllo [Imposta programmi predefiniti](../shell/default-programs.md) se si vuole consentire agli utenti dell'app di accedere all'interfaccia utente di gestione predefinita (l'interfaccia utente di gestione all'interno dell'app non è più supportata)

        -   La chiamata a [IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) consente all'utente di accedere alla pagina del pannello di controllo '[Imposta programmi predefiniti](../shell/default-programs.md)' per l'app specificata

## <a name="tests"></a>Test

-   Eseguire un test per verificare che le app vengano registrate correttamente nel pannello di controllo Imposta programmi predefiniti
-   Eseguire un test per verificare che le app vengano registrate correttamente per essere visualizzate nell'elenco OpenWith per i tipi di file, gli schemi URI o entrambi, che si registrano per gestire
-   Eseguire un test per verificare che le nuove notifiche dell'app vengano visualizzate dopo l'installazione dell'app e che l'utente richiami un tipo di file, uno schema URI o entrambi, che l'app sia stata registrata per gestire

## <a name="resources"></a>Risorse

-   [Procedure consigliate per il tipo di file e le associazioni URI nelle applicazioni desktop di Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [Associazioni del tipo di file e presentazione della conferenza di compilazione AutoPlay](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 