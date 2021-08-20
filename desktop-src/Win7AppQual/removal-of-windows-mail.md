---
description: Rimozione di Windows Posta elettronica
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Rimozione di Windows Posta elettronica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2456fa5bdf9d981385f2b4832250358f7bfdab1b223aeb3658d8df4cc212237b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328935"
---
# <a name="removal-of-windows-mail"></a>Rimozione di Windows Posta elettronica

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Alta  
**Frequenza** - Alta  









## <a name="description"></a>Descrizione

Microsoft sta deprecando l'Windows Mail e disabilitando l'API CoStartOutlookExpress. Le altre API di posta elettronica sono state contrassegnate come deprecate e devono essere rimosse in una versione Windows successiva. Tuttavia, le API documentate pubblicamente che non sono contrassegnate come deprecate o obsolete continueranno a funzionare in Windows 7. I file binari rimarranno nei sistemi degli utenti e continueranno a essere accessibili tramite le API, in particolare nei casi indicati in precedenza. Inoltre, i file di posta elettronica (con estensione eml) e di notizie (con estensione nws) degli utenti rimarranno nel sistema.

## <a name="manifestation-of-impact"></a>Impatto significativo

La rimozione Windows Mail comporta quanto segue:

-   Tutti i punti di ingresso Windows Posta elettronica e Contatti (ad esempio, Menu Start, Collegamenti creati dall'utente, Start -> Esegui e così via) vengono rimossi o disabilitati. Alcune di queste vengono rimosse completamente, altre avranno esito negativo durante il tentativo di avvio.
-   Tutte le DLL vengono spedite nella scatola
-   Le API documentate pubblicamente continuano a funzionare come in Windows Vista
-   Tutte le API che tentano di avviare l'interfaccia utente principale del browser sono state modificate per creare un errore invisibile all'utente. La funzione restituirà l'esito positivo, ma non mostrerà l'interfaccia utente all'utente. Le API che chiamano altre finestre di dialogo, ad esempio lo Spooler o la finestra di dialogo Account, continuano a mostrare tale interfaccia utente
-   I gestori di protocollo (mailto, ldap, news, snews, nntp) non verranno associati Windows Mail o Contacts. Quando tentano di avviarli, i clienti visualizzano una finestra di dialogo di errore che li indica alla posizione in cui possono impostare queste associazioni su un altro programma
-   Le associazioni di file (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) sono interrotte o disabilitate. Quando tentano di aprire un file con queste estensioni, i clienti otterrà una finestra di dialogo che offre loro altre app installate che possono usare e che puntano a una pagina Web che offre soluzioni
-   Tutti i file utente (ad esempio, i file di contatto o i messaggi) rimangono nel sistema nello scenario di aggiornamento
-   La cartella Contatti è nascosta per impostazione predefinita, quindi i clienti non la visualizzano
-   Le API sono contrassegnate come deprecate in MSDN
-   La funzione di anteprima del file è stata rimossa
-   Gli hook della shell nel menu di scelta rapida vengono rimossi
-   La funzione di ricerca file è stata rimossa

## <a name="mitigation"></a>Strategia di riduzione del rischio

Gli utenti devono installare Windows Live Mail o qualsiasi altro prodotto di posta elettronica in grado di leggere i file con estensione eml e nws.

## <a name="solution"></a>Soluzione

Rilevare se è installato un gestore di posta elettronica predefinito. In caso contrario, consigliare all'utente di installare Windows Live Mail o qualsiasi altro prodotto in grado di leggere i file con estensione eml e nws.

Non progettare codice che chiama l Windows aPI dell'interfaccia utente di Posta elettronica perché non funzionerà. È necessario trovare altri modi per accedere ai file con estensione eml e nws. Inoltre, non appena possibile, interrompere l'affidamento su tutte le altre API Windows Mail.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

-   Esercizio dell'applicazione in un ambiente Windows 7 per assicurarsi che l'applicazione non provi a chiamare l'API dell'interfaccia utente.
-   In alternativa, è possibile eseguire Application Compatibility Toolkit (ACT) usando Windows Compatibility Evaluator (WCE) per individuare eventuali problemi potenziali dovuti alla deprecazione di questa funzionalità.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[Application Compatibility Toolkit Download](/windows-hardware/get-started/adk-install)  
</dl>

 

 
