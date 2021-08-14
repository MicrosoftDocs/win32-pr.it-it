---
description: Azioni da parte di pacchetti di sicurezza non supportati in Windows.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce9f2d81a0a724d232e39c6e6fd7565b946ca319ba9f134041f6865b4bb2450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918907"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza

La rimozione, la sostituzione o il wrapping dei pacchetti di sicurezza della posta in arrivo (ad esempio, Kerberos o NTLM) non è un'azione supportata in Windows e a partire dal 10 gennaio 2017 non è consentita. È possibile aggiungere pacchetti di sicurezza di terze parti. tuttavia, Windows non supporta la rimozione di SSP/APs preconfigurati. In particolare, la modifica dell'impostazione del Registro di sistema **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ OSConfig \\ Security Packages** non è mai stata supportata.

A partire da Windows 8.1, i clienti che vogliono fornire funzionalità aggiuntive possono aggiungere i propri pacchetti di sicurezza usando l'impostazione del Registro di sistema **HKLM \\ SYSTEM \\ CurrentControlSet Control \\ \\ Lsa \\ Security Packages** ([Registering SSP/AP DLLs](registering-ssp-ap-dlls.md)) e l'impostazione del Registro di sistema **associata SecurityProviders** ([Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md)), se applicabile. Inoltre, lo [](../secgloss/s-gly.md#_security_security_package_gly) scopo dei pacchetti  di sicurezza è implementare nuovi protocolli di sicurezza che possono essere sotto forma di un provider di supporto per la sicurezza (SSP) o di un pacchetto [di](../secgloss/a-gly.md#_security_authentication_package_gly) autenticazione (AP). Lo scopo di un provider di servizi di configurazione  è fornire la connessione autenticata, l'integrità dei messaggi  e i servizi di crittografia dei messaggi che non sono già supportati nel sistema, mentre un punto di accesso viene usato per aggiungere una nuova logica di autenticazione usata per determinare se consentire a un utente di accedere. 

Microsoft ha investito nella sicurezza dei clienti e sta cercando di garantire che i processi critici, ad esempio i punti di accesso e i punti di accesso, non siano facilmente rimovibili dal sistema. Di conseguenza, l'impostazione del Registro di sistema **\\ HKLM SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ OSConfig \\ Security Packages** è stata limitata a partire da Windows 8.1 per impedire modifiche. Per facilitare i pacchetti di sicurezza di terze parti, i pacchetti di sicurezza **\\ HKLM SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\** sono stati resi l'impostazione designata per i provider di servizi di sicurezza/provider di servizi di sicurezza personalizzati. È inoltre consigliabile rimuovere da tali SSP/APs personalizzati tutte le funzionalità dei provider di servizi di sicurezza/provider di servizi di sicurezza personalizzati che non rientra nell'ambito dei pacchetti di sicurezza definiti da Microsoft e che i pacchetti di sicurezza della posta in arrivo non vengono rimossi da alcun prodotto.

 

 
