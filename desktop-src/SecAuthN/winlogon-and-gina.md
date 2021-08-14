---
description: Winlogon, l'APPLICAZIONE e i provider di rete sono le parti del modello di accesso interattivo.
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon e LANA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cc39b905d6a49eb84ccab164f99481561133e6cdd9ea40cfd0b1067315569a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915070"
---
# <a name="winlogon-and-gina"></a>Winlogon e LANA

[*Winlogon*](../secgloss/w-gly.md), [*i provider di rete e DIA*](../secgloss/g-gly.md)sono le parti del modello di accesso interattivo. La procedura di accesso interattivo è in genere controllata dai provider di rete, MSGina.dll e Winlogon. Per modificare la procedura di accesso interattivo, MSGina.dll può essere sostituito con una DLL DELL'APPLICAZIONE personalizzata.

Per usare Winlogon, i provider DI AUTENTICAZIONE e di rete, è necessario avere una solida conoscenza dell'architettura di sicurezza di Windows, in particolare per quanto riguarda [*i token,*](../secgloss/a-gly.md)i pacchetti di autenticazione e gli aspetti correlati. [](../secgloss/a-gly.md)

> [!Note]  
> Le DLL DELL'APPLICAZIONE vengono ignorate in Windows Vista.

 

Per informazioni su funzioni e strutture specifiche, vedere Riferimento [per l'autenticazione.](authentication-reference.md) Questa sezione di riferimento include le descrizioni delle funzioni che devono essere implementate da una DLL DELL'applicazione WINLOGOA, le funzioni di supporto winlogon che possono essere chiamate dalla DLL DELL'APPLICAZIONE e le strutture di dati usate per passare informazioni tra Winlogon e l'APPLICAZIONE.

Il codice DELLA di esempio è disponibile in Platform Software Development Kit (SDK) Security samples (Esempi di sicurezza di Platform Software Development Kit (SDK). Gli esempi contengono codice C per l'implementazione di uno stub e di un hook DELLA. Per altre informazioni sullo sviluppo di DLL DELL'APPLICAZIONE PERSONALIZZATA, inviare un messaggio di posta elettronica a: ginareqs@microsoft.com .

Per informazioni sul modello di autenticazione supportato da Windows e per informazioni dettagliate [](../secgloss/a-gly.md) sui servizi dell'autorità di sicurezza locale [](../secgloss/l-gly.md) (LSA) e sulle interfacce del pacchetto di autenticazione, vedere Autenticazione [LSA.](lsa-authentication.md)

Per informazioni sugli aspetti dell'autorità di sicurezza locale correlati all'amministrazione dei criteri di sicurezza, che include relazioni di trust con altri computer e domini, assegnazione di privilegi, controllo di generazione di controllo, accessibilità del sistema e altri argomenti simili, vedere [Criteri LSA.](../secmgmt/lsa-policy.md)

Per informazioni su Winlogon e LANA, vedere gli argomenti seguenti.



| Argomento                                                                              | Descrizione                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | Winlogon fornisce un set di funzioni di supporto per la DLL DELL'applicazione.<br/>                                                                                                                                                                 |
| [Gina](gina.md)                                                                   | Una DLL DELLA fornisce procedure di identificazione e autenticazione utente personalizzabili.<br/>                                                                                                                                            |
| [Funzioni DISA di Servizi terminal](terminal-services-gina-functions.md)           | Quando Servizi terminal è abilitato, l'APPLICAZIONE deve chiamare le funzioni di supporto winlogon per completare diverse attività.<br/>                                                                                                                   |
| [Interazione con i provider di rete](interaction-with-network-providers.md)       | È possibile configurare un sistema per supportare zero o più provider di rete.<br/>                                                                                                                                                          |
| [Responsabilità e funzionalità](responsibilities-and-features.md)                 | Ogni parte del processo di accesso interattivo ha un set di responsabilità.<br/>                                                                                                                                                      |
| [Interazione tra Winlogon e ILVA](interaction-between-winlogon-and-gina.md) | Lo stato di Winlogon determina quale funzione DELL'applicazione viene chiamata per elaborare qualsiasi evento [*di*](../secgloss/s-gly.md) sequenza di attenzione sicura (SAS) specificato.<br/> |
| [Pacchetti di notifica Winlogon](winlogon-notification-packages.md)               | È possibile implementare un pacchetto di notifica per monitorare e rispondere agli eventi Winlogon.<br/>                                                                                                                                            |



 

 

 
