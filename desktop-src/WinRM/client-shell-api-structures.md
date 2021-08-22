---
title: Strutture e definizioni delle API della shell client
description: La tabella seguente offre una panoramica delle strutture e di altre definizioni per l Windows API della shell client di gestione remota Windows (WinRM).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9c3d1f6f9f9d476e9b49ef309e5236e4421e0b5afa77fa1072b92f2060cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643261"
---
# <a name="client-shell-api-structures-and-definitions"></a>Strutture e definizioni delle API della shell client

La tabella seguente offre una panoramica delle strutture e di altre definizioni per l Windows API della shell client di gestione remota Windows (WinRM).



| Funzione                                                                      | Descrizione                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**FUNZIONE DI COMPLETAMENTO DELLA SHELL WSMAN \_ \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | Funzione di callback chiamata per le operazioni della shell, che comporta una richiesta remota. |



 



| Struttura                                                                      | Descrizione                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**CREDENZIALI DI \_ AUTENTICAZIONE \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Definisce il metodo di autenticazione e le credenziali utilizzate per l'autenticazione server o proxy.                                              |
| [**DATI \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Archivia i dati in ingresso e in uscita usati nell'API WinRM.                                                                                     |
| [**WSMAN \_ DATA \_ BINARY**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Archivia i dati binari da usare con varie funzioni dell'API WinRM.                                                                                |
| [**WSMAN \_ DATA \_ TEXT**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Archivia i dati basati su testo per l'uso con varie funzioni dell'API WinRM.                                                                            |
| [**VARIABILE DI AMBIENTE \_ \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Definisce una singola variabile di ambiente usando una coppia nome/valore.                                                                  |
| [**SET DI VARIABILI DI AMBIENTE WSMAN \_ \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Definisce una matrice di variabili di ambiente.                                                                                                  |
| [**ERRORE \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Contiene informazioni sull'errore.                                                                                                                 |
| [**CHIAVE \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Rappresenta una coppia chiave-valore all'interno di un set di selettori e viene usata per identificare una determinata risorsa.                                       |
| [**OPZIONE \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Rappresenta una coppia nome/valore dell'opzione specifica.                                                                                           |
| [**SET DI OPZIONI WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Rappresenta un set di opzioni.                                                                                                                |
| [**WSMAN \_ PROXY \_ INFO**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Imposta le informazioni sul proxy per ogni sessione.                                                                                                |
| [**WSMAN \_ RECEIVE \_ DATA \_ RESULT**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Rappresenta i dati di output ricevuti [**dall'API WSManReceiveShellOutput.**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)                                |
| [**DATI DI RISPOSTA WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Rappresenta i dati di output ricevuti da [**un'operazione WSMan.**](wsman.md)                                                                |
| [**SET DI SELETTORI WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Definisce un set di chiavi che rappresentano l'identità di una risorsa.                                                                            |
| [**WSMAN \_ SHELL \_ ASYNC**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Definisce una struttura asincrona passata a tutte le operazioni della shell.                                                                   |
| [**WSMAN \_ SHELL \_ DISCONNECT \_ INFO**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | DA DEFINIRE                                                                                                                                         |
| [**INFORMAZIONI DI AVVIO DELLA SHELL WSMAN \_ \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Archivia tutti i dati specifici della shell necessari per creare una shell usando la chiamata del plug-in [**WSManCreateShell.**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) |
| [**SET DI \_ ID FLUSSO WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Elenca tutti i flussi usati per l'input o l'output per la shell e i comandi.                                                  |
| [**CREDENZIALI PASSWORD NOME UTENTE WSMAN \_ \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Definisce le credenziali utilizzate per l'autenticazione.                                                                                            |



 

 

 