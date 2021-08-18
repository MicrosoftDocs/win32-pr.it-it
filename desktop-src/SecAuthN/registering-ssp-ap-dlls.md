---
description: Dopo aver sviluppato una libreria a collegamento dinamico del provider di supporto per la sicurezza/pacchetto di autenticazione (DLL SSP/AP) contenente uno o più pacchetti di sicurezza personalizzati, è necessario registrarlo.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registrazione delle DLL SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6405dc5ddce32ad5e4d87ed44f9344240b491fdc0ea789c30d5475ac6e73aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919501"
---
# <a name="registering-sspap-dlls"></a>Registrazione delle DLL SSP/AP

Dopo aver sviluppato una libreria a collegamento dinamico del pacchetto di autenticazione del [*provider*](../secgloss/s-gly.md)di supporto della sicurezza / [](../secgloss/a-gly.md) (DLL SSP/AP) contenente uno o più pacchetti di sicurezza personalizzati, è necessario registrarlo. [](../secgloss/s-gly.md) A tale scopo, aggiungere il nome della DLL SSP/AP personalizzata ai dati del valore del Registro di sistema seguente:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Lsa** Security \\ **Packages**

I dati per questo valore del Registro di sistema sono un elenco dei nomi delle DLL SSP/AP, senza l'estensione ".dll". Il tipo di dati per questo elenco è **REG \_ MULTI \_ SZ,** quindi deve essere presente un carattere Null ('0') tra ogni nome \\ di DLL nell'elenco.

In genere, le DLL SSP/AP vengono archiviate nella directory %systemroot%/system32. Se si tratta del percorso della DLL SSP/AP personalizzata, non includere il percorso come parte del nome della DLL. Se, tuttavia, la DLL si trova in un percorso diverso, includere il percorso completo della DLL nel nome.

Ogni volta che il sistema viene avviato, l'LSA carica le DLL SSP/AP in questo elenco ed esegue la sequenza di inizializzazione descritta in Inizializzazione in modalità [LSA](lsa-mode-initialization.md).

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>Registrazione di un pacchetto di sicurezza personalizzato come provider di servizi condivisi TLS predefinito

Dopo aver sviluppato un provider di supporto per la sicurezza TLS personalizzato e averlo registrato come descritto in precedenza, è necessario registrarlo anche come "provider di servizi di sicurezza TLS predefinito". A tale scopo, popolare il nome del pacchetto del provider di servizi condivisi personalizzato nei dati del valore del Registro di sistema seguente:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Lsa** Default TLS \\ **SSP**

I dati per questo valore del Registro di sistema sono il nome del pacchetto di SSP, non il nome dll. Il tipo di dati per è **REG \_ SZ**.

Le applicazioni in modalità utente che usano "SSP TLS predefinito" useranno il valore predefinito registrato qui. Le applicazioni in modalità kernel o le applicazioni in modalità utente che usano "Microsoft Unified Security Protocol Provider" o altri nomi SSP TLS specifici non saranno influenzati da questa modifica.

> [!Note]  
> Queste informazioni del Registro di sistema riguardano solo le DLL SSP/AP. Per informazioni sulla registrazione dei provider di supporto per la sicurezza , vedere Scrittura e installazione di [un provider di supporto per la sicurezza](writing-and-installing-a-security-support-provider.md). Per informazioni sulle differenze tra le DLL SSP/AP e SSP, vedere [SSP/APs e SSP.](ssp-aps-versus-ssps.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
