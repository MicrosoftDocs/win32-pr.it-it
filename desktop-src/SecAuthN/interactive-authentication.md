---
description: L'autenticazione è interattiva quando viene richiesto all'utente di fornire informazioni di accesso. L'autorità di sicurezza locale (LSA) esegue un'autenticazione interattiva quando un utente esegue l'accesso tramite l'interfaccia utente GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticazione interattiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348061"
---
# <a name="interactive-authentication"></a>Autenticazione interattiva

L'autenticazione è interattiva quando viene richiesto all'utente di fornire informazioni di accesso. L' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) esegue un'autenticazione interattiva quando un utente esegue l'accesso tramite l'interfaccia utente [*Gina*](../secgloss/g-gly.md) . Nella figura seguente sono illustrate le parti di una tipica autenticazione interattiva.

![autenticazione interattiva](images/lsaint3.png)

Un utente segnala al sistema di avviare la sequenza di accesso digitando la firma di accesso condiviso (SAS, [*Secure Attention Sequence*](../secgloss/s-gly.md) ) CTRL + ALT + CANC. [*Winlogon*](../secgloss/w-gly.md) riceve la firma di accesso condiviso e chiama Gina per visualizzare un'interfaccia utente e ottenere i dati di accesso dell'utente, ad esempio un nome utente e una password.

Dopo aver ottenuto i dati di accesso, GINA chiama la funzione [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) per autenticare l'utente, specificando il pacchetto di autenticazione da usare per valutare i dati di accesso.

LSA chiama il pacchetto di autenticazione specificato e vi passa i dati di accesso. Il pacchetto di autenticazione esamina i dati e determina se l'autenticazione ha avuto esito positivo. Il risultato dell'autenticazione viene restituito a GINA da LSA e da LSA.

GINA Visualizza l'esito positivo o negativo dell'autenticazione per l'utente e restituisce il risultato dell'autenticazione a Winlogon. Se l'autenticazione ha esito positivo, viene avviata la sessione di accesso dell'utente e viene salvato un set di [*credenziali*](../secgloss/c-gly.md) di accesso per riferimento futuro.

> [!Note]  
> In generale, uno sviluppatore che scrive un oggetto GINA personalizzato per accettare dati di accesso specializzati, ad esempio una [*Smart Card*](../secgloss/s-gly.md) o dati di analisi retinica, deve anche scrivere un pacchetto di autenticazione responsabile dell'elaborazione dei dati e della relativa autenticità.

 

Per ulteriori informazioni su Winlogon e GINA, vedere [Winlogon e Gina](winlogon-and-gina.md). Per ulteriori informazioni sui pacchetti di autenticazione, vedere [creazione di pacchetti di sicurezza personalizzati](creating-custom-security-packages.md).

 

 
