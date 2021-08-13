---
description: L'autenticazione è interattiva quando a un utente viene richiesto di specificare le informazioni di accesso. L'autorità di sicurezza locale (LSA) esegue un'autenticazione interattiva quando un utente accede tramite l'interfaccia utente DIA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticazione interattiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876f3aced39afba0d08a9643e14caae91336daf38a63f3855e76fe50136a16a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482296"
---
# <a name="interactive-authentication"></a>Autenticazione interattiva

L'autenticazione è interattiva quando a un utente viene richiesto di specificare le informazioni di accesso. [*L'autorità di sicurezza*](../secgloss/l-gly.md) locale (LSA) esegue un'autenticazione interattiva quando un utente accede tramite l'interfaccia utente [*DIA.*](../secgloss/g-gly.md) La figura seguente illustra le parti di una tipica autenticazione interattiva.

![autenticazione interattiva](images/lsaint3.png)

Un utente segnala al sistema di iniziare la sequenza [](../secgloss/s-gly.md) di accesso digitando CTRL+ALT+CANC. [*Winlogon*](../secgloss/w-gly.md) riceve la firma di accesso condiviso e chiama GINA per visualizzare un'interfaccia utente e ottenere i dati di accesso dell'utente, ad esempio un nome utente e una password.

Dopo aver ottenuto i dati di accesso, GINA chiama la funzione [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) per autenticare l'utente, specificando il pacchetto di autenticazione da usare per valutare i dati di accesso.

LSA chiama il pacchetto di autenticazione specificato e passa i dati di accesso. Il pacchetto di autenticazione esamina i dati e determina se l'autenticazione ha esito positivo. Il risultato dell'autenticazione viene restituito all'LSA e dall'LSA all'istanza di GINA.

GINA visualizza l'esito positivo o negativo dell'autenticazione per l'utente e restituisce il risultato dell'autenticazione a Winlogon. Se l'autenticazione ha esito positivo, viene avviata la [](../secgloss/c-gly.md) sessione di accesso dell'utente e viene salvato un set di credenziali di accesso per riferimento futuro.

> [!Note]  
> In [*generale,*](../secgloss/s-gly.md) uno sviluppatore che scrive un file GINA personalizzato per accettare dati di accesso specializzati, ad esempio dati di smart card o di analisi retinale, deve anche scrivere un pacchetto di autenticazione responsabile dell'elaborazione dei dati e della relativa autenticità.

 

Per altre informazioni su Winlogon e GINA, vedere [Winlogon e GINA.](winlogon-and-gina.md) Per altre informazioni sui pacchetti di autenticazione, vedere [Creazione di pacchetti di sicurezza personalizzati.](creating-custom-security-packages.md)

 

 
