---
description: Dopo aver sviluppato una libreria di collegamento dinamico (SSP/AP) del pacchetto di Security Support Provider/autenticazione contenente uno o più pacchetti di sicurezza personalizzati, è necessario registrarla.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registrazione di dll SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756425"
---
# <a name="registering-sspap-dlls"></a>Registrazione di dll SSP/AP

Dopo lo sviluppo [](../secgloss/s-gly.md)di una / libreria di collegamento dinamico (SSP/AP) del [*pacchetto di autenticazione*](../secgloss/a-gly.md) Security Support Provider contenente uno o più pacchetti di [*sicurezza*](../secgloss/s-gly.md)personalizzati, è necessario registrarla. A tale scopo, aggiungere il nome della DLL SSP/AP personalizzata ai dati del valore del registro di sistema seguente:

**HKEY \_ \_** Pacchetti di \\  \\  \\  \\  \\ **sicurezza** LSA per il controllo CurrentControlSet di sistema del computer locale

I dati per questo valore del registro di sistema sono un elenco dei nomi di dll SSP/AP, senza l'estensione "dll". Il tipo di dati per questo elenco **è \_ reg \_ multisz** , quindi deve essere presente un carattere null (' \\ 0') tra ogni nome di dll presente nell'elenco.

In genere, le dll SSP/AP sono archiviate nella directory% SystemRoot%/system32. Se questo è il percorso della DLL SSP/AP personalizzata, non includere il percorso come parte del nome della DLL. Se, tuttavia, la DLL si trova in un percorso diverso, includere il percorso completo della DLL nel nome.

Ogni volta che il sistema viene avviato, LSA carica le dll SSP/AP in questo elenco ed esegue la sequenza di inizializzazione descritta nell' [inizializzazione in modalità LSA](lsa-mode-initialization.md).

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>Registrazione di un pacchetto di sicurezza personalizzato come SSP TLS predefinito

Dopo aver sviluppato un Security Support Provider TLS personalizzato e averlo registrato come descritto in precedenza, è necessario registrarlo anche come "SSP TLS predefinito". A tale scopo, popolare il nome del pacchetto SSP personalizzato con i dati del valore del registro di sistema seguente:

**HKEY \_ \_** \\  \\  \\  \\  \\ **SSP TLS predefinito** del sistema CurrentControlSet del computer locale

I dati per questo valore del registro di sistema sono il nome del pacchetto SSP, non il nome della dll. Il tipo di dati per è **reg \_ SZ**.

Le applicazioni in modalità utente che usano "SSP TLS predefinito" utilizzeranno il valore predefinito registrato qui. Questa modifica non avrà alcun effetto sulle applicazioni in modalità kernel o sulle applicazioni in modalità utente che usano "provider del protocollo di sicurezza unificato Microsoft" o altri nomi di SSP TLS specifici.

> [!Note]  
> Le informazioni del registro di sistema riguardano solo le DLL SSP/AP. Per informazioni sulla registrazione dei provider di supporto per la sicurezza (SSP), vedere [scrittura e installazione di un Security Support Provider](writing-and-installing-a-security-support-provider.md). Per informazioni sulle differenze tra le dll SSP/AP e SSP, vedere [SSP/APS](ssp-aps-versus-ssps.md)e SSP.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
