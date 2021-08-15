---
description: Il Windows operativo supporta l'autenticazione tramite pacchetti di sicurezza che funzionano sia come provider di supporto per la sicurezza che come pacchetti di autenticazione.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Provider di supporto per la sicurezza/Pacchetti di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62f634d0571eab43652485f8ca1313f78fd157ca202d5d78369552db648de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918340"
---
# <a name="security-support-providerauthentication-packages"></a>Provider di supporto per la sicurezza/Pacchetti di autenticazione

Il Windows operativo supporta l'autenticazione [](../secgloss/s-gly.md) tramite pacchetti di sicurezza che funzionano sia come provider di supporto per la [*sicurezza*](../secgloss/s-gly.md) che come pacchetti [*di autenticazione*](../secgloss/a-gly.md). I pacchetti di sicurezza forniscono i servizi di supporto del processo di accesso di un pacchetto di autenticazione Windows e forniscono servizi di autenticazione alle applicazioni implementando un set di funzioni mappate a [SSPI (Security Support Provider Interface).](sspi.md)

Un pacchetto di sicurezza che funziona come pacchetto di autenticazione e implementa le funzionalità richieste da [*SSPI*](../secgloss/s-gly.md) è denominato provider di supporto della sicurezza/pacchetto di autenticazione (SSP/AP).

Per altre informazioni sui pacchetti di sicurezza, vedere [Pacchetti SSP forniti da Microsoft.](ssp-packages-provided-by-microsoft.md) Per informazioni sullo sviluppo di provider di servizi di configurazione/provider di servizi di accesso personalizzati, vedere [Pacchetti di sicurezza personalizzati.](custom-security-packages.md)

 

 
