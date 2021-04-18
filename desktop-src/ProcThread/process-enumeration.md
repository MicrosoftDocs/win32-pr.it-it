---
description: Tutti gli utenti hanno accesso in lettura all'elenco di processi nel sistema e sono disponibili diverse funzioni che enumerano i processi attivi. La funzione da usare dipende da fattori quali il supporto della piattaforma desiderata.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Elaborazione enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311968"
---
# <a name="process-enumeration"></a>Elaborazione enumerazione

Tutti gli utenti hanno accesso in lettura all'elenco di processi nel sistema e sono disponibili diverse funzioni che enumerano i processi attivi. La funzione da usare dipende da fattori quali il supporto della piattaforma desiderata.

Le funzioni seguenti vengono utilizzate per enumerare i processi.



| Funzione                                                    | Descrizione                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Recupera l'identificatore di processo per ogni oggetto processo nel sistema.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Recupera le informazioni sul primo processo rilevato in uno snapshot del sistema.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Recupera le informazioni sul processo successivo registrato in uno snapshot del sistema.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Recupera le informazioni sui processi attivi sul server terminal specificato. |



 

Le funzioni TOOLHELP e [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerano tutti i processi. Per elencare i processi in esecuzione in un account utente specifico, usare [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) e filtrare nel SID utente. È possibile filtrare l'ID sessione per nascondere i processi in esecuzione in altre sessioni di Terminal Server.

È anche possibile filtrare i processi in base all'account utente, indipendentemente dalla funzione di enumerazione, chiamando [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)e [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con **TokenUser**. Tuttavia, non è possibile aprire un processo protetto da un descrittore di sicurezza a meno che non sia stato concesso l'accesso.

 

 
