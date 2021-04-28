---
description: Rimozione di Windows Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Rimozione di Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116279"
---
# <a name="removal-of-windows-mail"></a>Rimozione di Windows Mail

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Alta  
**Frequenza** - Alta  









## <a name="description"></a>Descrizione

Microsoft sta deprecando l'utilità Windows Mail e disabilitando l'API CoStartOutlookExpress. Le altre API di posta elettronica sono state contrassegnate come deprecate e sono programmate per la rimozione in una versione successiva di Windows. Tuttavia, le API documentate pubblicamente che non sono contrassegnate come deprecate o obsolete continueranno a funzionare in Windows 7. I file binari rimarranno nei sistemi degli utenti e continueranno a essere accessibili tramite le API, in particolare nei casi indicati in precedenza. Inoltre, i file di posta elettronica (.eml) e di notizie (con estensione nws) degli utenti rimarranno nel sistema.

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

La rimozione di Windows Mail comporta quanto segue:

-   Tutti i punti di ingresso a Windows Mail e Ai contatti (ad esempio, Menu Start, Collegamenti creati dall'utente, Avvia -> Esegui e così via) vengono rimossi o disabilitati. Alcune di queste vengono rimosse completamente, altre avranno esito negativo durante il tentativo di avvio.
-   Tutte le DLL vengono spedite nella casella
-   Le API documentate pubblicamente continuano a funzionare come in Windows Vista
-   Tutte le API che tentano di avviare l'interfaccia utente principale del browser sono state modificate per creare un errore invisibile all'utente. La funzione restituirà l'esito positivo, ma non mostrerà l'interfaccia utente all'utente. Le API che chiamano altre finestre di dialogo, ad esempio lo Spooler o la finestra di dialogo Account, continuano a mostrare tale interfaccia utente
-   I gestori di protocollo (mailto, ldap, news, snews, nntp) non verranno associati a Windows Mail o Contatti. Quando tentano di avviarli, i clienti visualizzano una finestra di dialogo di errore che li indica alla posizione in cui possono impostare queste associazioni su un altro programma
-   Le associazioni di file (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) sono interrotte o disabilitate. Quando tentano di aprire un file con queste estensioni, i clienti otterrà una finestra di dialogo che offre loro altre app installate che possono usare e che puntano a una pagina Web che offre soluzioni
-   Tutti i file utente (ad esempio, i file di contatto o i messaggi) rimangono nel sistema nello scenario di aggiornamento
-   La cartella Contatti è nascosta per impostazione predefinita, quindi i clienti non la visualizzano
-   Le API sono contrassegnate come deprecate in MSDN
-   La funzione di anteprima del file è stata rimossa
-   Gli hook della shell nel menu di scelta rapida vengono rimossi
-   La funzione di ricerca file è stata rimossa

## <a name="mitigation"></a>Mitigazione

Gli utenti devono installare Windows Live Mail o qualsiasi altro prodotto di posta elettronica in grado di leggere i file con estensione eml e nws.

## <a name="solution"></a>Soluzione

Rilevare se è installato un gestore di posta elettronica predefinito. In caso contrario, consigliare all'utente di installare Windows Live Mail o qualsiasi altro prodotto in grado di leggere i file con estensione eml e nws.

Non progettare codice che chiama l'API dell'interfaccia utente di Windows Mail, perché non funzionerà. È necessario trovare altri modi per accedere ai file con estensione eml e nws. Inoltre, non appena è possibile, interrompere l'affidamento su tutte le altre API di Windows Mail.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

-   Eseguire l'applicazione in un ambiente Windows 7 per assicurarsi che l'applicazione non tuffi a chiamare l'API dell'interfaccia utente.
-   In alternativa, è possibile eseguire Application Compatibility Toolkit (ACT) usando Windows Compatibility Evaluator (WCE) per individuare eventuali problemi potenziali dovuti alla deprecazione di questa funzionalità.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[Application Compatibility Toolkit Download](/windows-hardware/get-started/adk-install)  
</dl>

 

 
