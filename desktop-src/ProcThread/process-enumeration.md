---
description: Tutti gli utenti hanno accesso in lettura all'elenco dei processi nel sistema e sono disponibili diverse funzioni che enumerano i processi attivi. La funzione da usare dipende da fattori come il supporto della piattaforma desiderato.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Enumerazione Process
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05caa13d0f53fc87828669b2e19eba126c62c28f492b2f41d09caf2377321a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081321"
---
# <a name="process-enumeration"></a>Enumerazione Process

Tutti gli utenti hanno accesso in lettura all'elenco dei processi nel sistema e sono disponibili diverse funzioni che enumerano i processi attivi. La funzione da usare dipende da fattori come il supporto della piattaforma desiderato.

Le funzioni seguenti vengono usate per enumerare i processi.



| Funzione                                                    | Descrizione                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Recupera l'identificatore di processo per ogni oggetto processo nel sistema.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Recupera informazioni sul primo processo rilevato in uno snapshot di sistema.    |
| [**Processo32Avanti**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Recupera informazioni sul processo successivo registrato in uno snapshot di sistema.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Recupera informazioni sui processi attivi nel server terminal specificato. |



 

Le funzioni toolhelp ed [**EnumProcesses enumerano**](/windows/win32/api/psapi/nf-psapi-enumprocesses) tutti i processi. Per elencare i processi in esecuzione in un account utente specifico, utilizzare [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) e filtrare in base al SID utente. È possibile filtrare in base all'ID sessione per nascondere i processi in esecuzione in altre sessioni del server terminal.

È anche possibile filtrare i processi in base all'account utente, indipendentemente dalla funzione di enumerazione, chiamando [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)e [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con **TokenUser**. Tuttavia, non è possibile aprire un processo protetto da un descrittore di sicurezza a meno che non sia stato concesso l'accesso.

 

 
