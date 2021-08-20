---
title: Modello di associazioni di tipo di file e URI
description: Modello di associazioni di tipo di file e URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabcdb40bd38aeee24ee0e5d86f11651633a7eead1748810e8c1c6a846827690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028859"
---
# <a name="file-type-and-uri-associations-model"></a>Modello di associazioni di tipo di file e URI

## <a name="platforms"></a>Piattaforme

 **Client** - Windows 8  
**Server** - Windows Server 2012  



## <a name="description"></a>Descrizione

Il tipo di file e il modello di associazione URI sono stati modificati in Windows 8. Le app non possono più impostare se stesse a livello di codice come gestore predefinito per un tipo di file o un URI. Ora invece l'utente controlla sempre qual è il gestore predefinito per un tipo di file o uno schema URI.

## <a name="manifestation"></a>Manifestazione

Il modo in cui questa modifica viene presentata all'utente dipende dalla modalità di progettazione dell'app, ad esempio:

-   Molte app verificano se sono le impostazioni predefinite a ogni esecuzione e, in caso contrario, chiederanno all'utente di impostarle come predefinite. Tuttavia, poiché le app non possono più eseguire query accurate per determinare quale app è il gestore predefinito per un tipo di file o uno schema URI, nessuna di queste operazioni funziona.
-   Molte app hanno una finestra di dialogo o un menu incorporato o nel programma di installazione che specifica i tipi di file per cui l'app deve fungere da impostazione predefinita. Tuttavia, poiché le app non possono più impostarsi a livello di codice come gestore predefinito per un tipo di file o uno schema URI, questo non funziona più.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli utenti possono eseguire diverse operazioni per gestire queste modifiche:

-   Agli utenti viene richiesto contestualmente di scegliere un'app predefinita per gestire tipi di file, schemi URI o entrambi quando non ne è stata specificata una
-   Agli utenti viene offerta la possibilità di modificare il gestore predefinito dopo l'installazione di nuove app in grado di gestire un tipo di file o uno schema URI
-   Il pannello di controllo dei programmi predefiniti consente agli utenti di impostare i valori predefiniti per un'app o per un tipo di file, uno schema URI o entrambi. le app possono collegarsi al pannello di controllo
-   Le impostazioni predefinite possono essere modificate da Windows Explorer

## <a name="solution"></a>Soluzione

In seguito a queste modifiche, vengono fornite le linee guida per le API seguenti:

-   La funzionalità di alcune chiamate al metodo all'interno dell'API [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) è cambiata e non deve più essere usata.

    -   **Non chiamare** [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) per determinare se un'app è l'impostazione predefinita
    -   **Non chiamare** [QueryCurrentDefault per](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) determinare quale app (se presente) è l'impostazione predefinita corrente
    -   **Non chiamare** [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) per impostare l'app predefinita

-   Le linee guida per il futuro sono:

    -   **Non eseguire** query per vedere quale app è il gestore predefinito per i tipi di file o gli schemi URI

    -   **Non tentare di** monitorare le modifiche nel gestore predefinito per i tipi di file o gli schemi URI

    -   **Non tentare di** impostare un'app come gestore predefinito per i tipi di file o gli schemi URI

    -   **Non tentare di** gestire le impostazioni predefinite per i tipi di file o gli schemi URI dall'interno di un'app

    -   **Eseguire** l'integrazione con [il](../shell/default-programs.md) pannello di controllo Imposta programmi predefiniti se si vuole consentire agli utenti dell'app di accedere all'interfaccia utente di gestione predefinita (l'interfaccia utente di gestione all'interno dell'app non è più supportata)

        -   La [chiamata a IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) consente all'utente di accedere alla pagina del pannello di controllo['Imposta](../shell/default-programs.md)programmi predefiniti' per l'app specificata

## <a name="tests"></a>Test

-   Testare per verificare che le app si registrino correttamente nel pannello di controllo Imposta programmi predefiniti
-   Testare per verificare che le app si registrino correttamente per essere visualizzate nell'elenco OpenWith per i tipi di file, gli schemi URI o entrambi, che registrano per gestire
-   Testare per verificare che vengano visualizzate nuove notifiche dell'app dopo l'installazione dell'app e che l'utente richiama un tipo di file, uno schema URI o entrambi, che l'app ha registrato per gestire

## <a name="resources"></a>Risorse

-   [Procedure consigliate per il tipo di file e le associazioni URI nelle Windows 8 desktop](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [Presentazione della conferenza associazioni dei tipi di file e compilazione AutoPlay](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 