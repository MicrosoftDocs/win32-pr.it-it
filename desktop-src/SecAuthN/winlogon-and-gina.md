---
description: Winlogon, GINA e i provider di rete sono le parti del modello di accesso interattivo.
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon e GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a683077f275dc9bf38efca6649cbd8131e0b9334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879037"
---
# <a name="winlogon-and-gina"></a>Winlogon e GINA

[*Winlogon*](../secgloss/w-gly.md), [*Gina*](../secgloss/g-gly.md)e i provider di rete sono le parti del modello di accesso interattivo. La procedura di accesso interattivo è generalmente controllata da Winlogon, MSGina.dll e provider di rete. Per modificare la procedura di accesso interattivo, è possibile sostituire MSGina.dll con una DLL personalizzata GINA.

Per lavorare con Winlogon, i provider GINA e i provider di rete, è necessario avere una conoscenza approfondita dell'architettura di sicurezza di Windows, in particolare per quanto riguarda i [*token*](../secgloss/a-gly.md), i [*pacchetti di autenticazione*](../secgloss/a-gly.md)e gli argomenti correlati.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Per informazioni sulle funzioni e sulle strutture specifiche, vedere [riferimento per l'autenticazione](authentication-reference.md). Questa sezione di riferimento include le descrizioni delle funzioni che devono essere implementate da una DLL GINA, le funzioni di supporto di Winlogon che la DLL GINA può chiamare e le strutture di dati usate per passare le informazioni tra Winlogon e GINA.

Il codice GINA di esempio è disponibile nella pagina relativa agli esempi di sicurezza di Platform Software Development Kit (SDK). Gli esempi contengono codice C per implementare uno stub GINA e un hook GINA. Per ulteriori informazioni sullo sviluppo personalizzato di DLL GINA, inviare un messaggio di posta elettronica a: ginareqs@microsoft.com .

Per informazioni sul modello di autenticazione supportato da Windows e per informazioni dettagliate sui servizi dell' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) e sulle interfacce del [*pacchetto di autenticazione*](../secgloss/a-gly.md) , vedere [LSA Authentication](lsa-authentication.md).

Per informazioni sugli aspetti dell'autorità di sicurezza locale che riguardano l'amministrazione dei criteri di sicurezza, incluse le relazioni di trust con altri computer e domini, l'assegnazione dei privilegi, il controllo della generazione del controllo, l'accessibilità del sistema e altri argomenti simili, vedere la pagina relativa ai [criteri LSA](../secmgmt/lsa-policy.md).

Per informazioni su Winlogon e GINA, vedere gli argomenti seguenti.



| Argomento                                                                              | Descrizione                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | Winlogon fornisce un set di funzioni di supporto per la DLL GINA.<br/>                                                                                                                                                                 |
| [GINA](gina.md)                                                                   | Una DLL GINA fornisce le procedure di autenticazione e identificazione utente personalizzabili.<br/>                                                                                                                                            |
| [Funzioni di Servizi terminal GINA](terminal-services-gina-functions.md)           | Quando i servizi Terminal sono abilitati, GINA deve chiamare le funzioni di supporto di Winlogon per completare diverse attività.<br/>                                                                                                                   |
| [Interazione con i provider di rete](interaction-with-network-providers.md)       | È possibile configurare un sistema per supportare zero o più provider di rete.<br/>                                                                                                                                                          |
| [Responsabilità e funzionalità](responsibilities-and-features.md)                 | Ogni parte del processo di accesso interattivo ha un set di responsabilità.<br/>                                                                                                                                                      |
| [Interazione tra Winlogon e GINA](interaction-between-winlogon-and-gina.md) | Lo stato di Winlogon determina quale funzione GINA viene chiamata per elaborare qualsiasi evento di firma di [*attenzione protetta*](../secgloss/s-gly.md) specificato.<br/> |
| [Pacchetti di notifica di Winlogon](winlogon-notification-packages.md)               | È possibile implementare un pacchetto di notifica per monitorare e rispondere agli eventi di Winlogon.<br/>                                                                                                                                            |



 

 

 
