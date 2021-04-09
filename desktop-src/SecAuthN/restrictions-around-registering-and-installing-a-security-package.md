---
description: Azioni per pacchetti di sicurezza non supportati in Windows.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd10cd8e2e98d4dccfc3a6230c3daecaeb8fec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749610"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza

La rimozione, la sostituzione o il wrapping dei pacchetti di sicurezza della posta in arrivo (ad esempio, Kerberos o NTLM) non è un'azione supportata in Windows e, a partire dal 10 gennaio 2017, viene impedito. È possibile aggiungere pacchetti di sicurezza di terze parti (SSP/APs); Tuttavia, Windows non supporta la rimozione di SSP/APs preconfigurati. In particolare, la modifica dell'impostazione del registro di **\\ sistema HKLM System \\ CurrentControlSet \\ Control \\ LSA \\ OSConfig \\ Security Packages** non è mai stata supportata.

A partire da Windows 8.1, i clienti che desiderano fornire funzionalità aggiuntive possono aggiungere i propri pacchetti di sicurezza usando l'impostazione del registro di **\\ sistema HKLM System \\ CurrentControlSet \\ Control \\ LSA \\ Security Packages** ([Registering SSP/AP DLLs](registering-ssp-ap-dlls.md)) e l'impostazione del registro di sistema associata **SecurityProviders** ([scrittura e installazione di un Security Support Provider](writing-and-installing-a-security-support-provider.md)), se applicabile. Inoltre, lo scopo dei [pacchetti di sicurezza](../secgloss/s-gly.md#_security_security_package_gly) consiste nell'implementare nuovi *protocolli di sicurezza* che possono essere sotto forma di Security Support Provider (SSP) o di un pacchetto di [autenticazione](../secgloss/a-gly.md#_security_authentication_package_gly) (AP). Lo scopo di un provider di servizi condivisi è fornire la *connessione autenticata*, l' *integrità dei messaggi* e i *servizi di crittografia dei messaggi* che non sono già supportati nel sistema, mentre un AP viene utilizzato per aggiungere la nuova *logica di autenticazione* utilizzata per determinare se consentire a un utente di effettuare l'accesso.

Microsoft viene investito nella sicurezza dei clienti e sta provando a garantire che i processi critici, ad esempio SSP e APs, non siano facilmente rimovibili dal sistema. Di conseguenza, l'impostazione del registro di **\\ sistema HKLM System \\ CurrentControlSet \\ Control \\ LSA \\ OSConfig \\ Security packages** è stata limitata a partire da Windows 8.1 per evitare modifiche. Per semplificare i pacchetti di sicurezza di terze parti, i **\\ pacchetti di sicurezza HKLM System \\ CurrentControlSet \\ Control \\ LSA \\** hanno reso l'impostazione designata per i provider di servizi condivisi/APS personalizzati. È inoltre consigliabile che tutte le funzionalità di SSP/APs personalizzati che esulano dall'ambito dei pacchetti di sicurezza definiti da Microsoft vengano rimosse da tali SSP/APs personalizzati e che i pacchetti di sicurezza della posta in arrivo non vengano rimossi da alcun prodotto.

 

 
