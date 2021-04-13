---
title: Strutture e definizioni dell'API della shell client
description: Nella tabella seguente viene fornita una panoramica delle strutture e di altre definizioni per l'API della shell client di Gestione remota Windows (WinRM).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00a908856a6df8233e377d917ff28029dc8468e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399180"
---
# <a name="client-shell-api-structures-and-definitions"></a>Strutture e definizioni dell'API della shell client

Nella tabella seguente viene fornita una panoramica delle strutture e di altre definizioni per l'API della shell client di Gestione remota Windows (WinRM).



| Funzione                                                                      | Descrizione                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_funzione di \_ completamento della shell WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | Funzione di callback chiamata per le operazioni della shell, che genera una richiesta remota. |



 



| Struttura                                                                      | Descrizione                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_credenziali di autenticazione WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Definisce il metodo di autenticazione e le credenziali utilizzate per l'autenticazione del server o del proxy.                                              |
| [**\_dati WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Archivia i dati in ingresso e in uscita utilizzati nell'API WinRM.                                                                                     |
| [**\_file binario dei dati WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Archivia i dati binari per l'utilizzo con varie funzioni API WinRM.                                                                                |
| [**\_testo dati \_ WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Archivia i dati basati su testo da usare con varie funzioni API WinRM.                                                                            |
| [**\_variabile di ambiente WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Definisce una singola variabile di ambiente utilizzando una coppia nome/valore.                                                                  |
| [**\_set di \_ variabili di ambiente WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Definisce una matrice di variabili di ambiente.                                                                                                  |
| [**\_errore WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Contiene informazioni sull'errore.                                                                                                                 |
| [**\_chiave WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Rappresenta una coppia chiave-valore all'interno di un set di selettori e viene utilizzata per identificare una determinata risorsa.                                       |
| [**\_opzione WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Rappresenta una coppia di nome e valore di opzione specifica.                                                                                           |
| [**\_set di opzioni WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Rappresenta un set di opzioni.                                                                                                                |
| [**\_informazioni sul proxy WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Imposta le informazioni sul proxy per ogni sessione.                                                                                                |
| [**\_ \_ risultato dati di ricezione WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Rappresenta i dati di output ricevuti dall'API [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput) .                                |
| [**\_dati di risposta WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Rappresenta i dati di output ricevuti da un'operazione [**WSMan**](wsman.md) .                                                                |
| [**\_set di selettori WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Definisce un set di chiavi che rappresentano l'identità di una risorsa.                                                                            |
| [**\_asincrono della shell WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Definisce una struttura asincrona passata a tutte le operazioni della shell.                                                                   |
| [**\_ \_ informazioni disconnessione Shell WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | TBD                                                                                                                                         |
| [**\_informazioni di \_ avvio della shell WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Archivia tutti i dati specifici della Shell necessari per creare una shell tramite la chiamata del plug-in [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) . |
| [**\_set di \_ ID \_ flusso WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Elenca tutti i flussi usati per l'input o l'output per la shell e i comandi.                                                  |
| [**\_nome utente WSMan \_ password \_ credenziali**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Definisce le credenziali utilizzate per l'autenticazione.                                                                                            |



 

 

 