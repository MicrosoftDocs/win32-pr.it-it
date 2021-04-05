---
title: Uso di TBS
description: Ogni comando inviato a TBS è associato a un'entità specifica. Questa operazione viene eseguita creando uno o più contesti per un'entità, che vengono quindi associati a ogni comando successivo Inviato da tale entità.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- Servizi di base TPM TBS, esempi
- Servizi di base TPM TBS, uso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955519"
---
# <a name="using-tbs"></a>Uso di TBS

La funzionalità Servizi di base TPM è divisa in quattro aree funzionali:

-   [Virtualizzazione delle risorse](resource-virtualization.md)
-   [Pianificazione comandi](command-scheduling.md)
-   [Risparmio energia](power-management.md)
-   [Blocco comandi](command-blocking.md)

Per assicurarsi che entità diverse non possano accedere alle risorse reciproche, ogni comando inviato a TBS è associato a un'entità specifica. Questa operazione viene eseguita creando uno o più contesti per un'entità, che vengono quindi associati a ogni comando successivo Inviato da tale entità. Ogni comando include un oggetto context, che consente a TBS di eseguire i comandi TPM nel contesto appropriato. Tutti gli oggetti creati dai comandi vengono scaricati dal TPM quando il contesto viene chiuso.

Un'entità crea il contesto prima di accedere prima a TBS e mantiene il contesto fino a quando non termina l'esecuzione degli accessi TBS. Ad esempio, nel caso di TSS, la funzionalità del servizio TCG Core Services (TCS) di TSS creerebbe un contesto di TBS all'avvio e manterrà il contesto attivo fino a quando non si arresta.

Per Windows Server 2008 e Windows Vista, TBS limita l'accesso all'API TBS agli account Administrators, NT AUTHORITY \\ LocalService e NT Authority \\ NetworkService. Per impostazione predefinita, questi account sono gli unici che possono connettersi a TBS e creare contesti. Le restrizioni di accesso possono essere modificate creando un **accesso** alla chiave del registro di sistema con un nome di valore del registro di sistema di stringa (**reg \_ SZ**) **securityDescriptor** <dl> <dt>

Tipo di dati
</dt> <dd>REG_SZ</dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

Esempio:

**O:BAG: BAD: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; LS**

Per impostazione predefinita, il numero massimo di contesti supportato da TBS è 25. Questo numero può essere modificato creando o modificando un valore **DWORD** del registro di sistema denominato **MaxContexts** in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**. È possibile osservare l'utilizzo del contesto di TBS in tempo reale usando lo strumento Performance Monitor per tenere traccia del numero di contesti TBS.

Per Windows 8, Windows Server 2012 e versioni successive, TBS consente l'accesso agli utenti e agli amministratori standard. Le chiavi del registro di sistema **securityDescriptor** e **MaxContexts** sono diventate obsolete. Per Windows 8, Windows Server 2012 e versioni successive, TBS limita l'accesso a determinati comandi usando il blocco dei comandi.

Per Windows 10, versione 1607, TBS consente l'accesso dalle applicazioni AppContainer. Per ogni versione del TPM, le chiavi **BlockedAppContainerCommands** e **AllowedW8AppContainerCommands** sono state aggiunte con gli elenchi corrispondenti rispettivamente dei comandi TPM bloccati e consentiti.

Per Windows 10, versione 1803, le chiavi del registro di sistema in **AllowedW8AppContainerCommands** non sono più supportate.

 

 




