---
description: Illustra le voci del Registro di sistema per gli eventi Winlogon.
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: Voci del Registro di sistema (autenticazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388cbe42d085543d5e7d4df1c9705504864b370cf94eb32f4025eaba12b89ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919447"
---
# <a name="registry-entries-authentication"></a>Voci del Registro di sistema (autenticazione)

Per consentire al pacchetto di ricevere notifiche degli eventi da [*Winlogon,*](../secgloss/w-gly.md)è necessario specificare il nome del pacchetto, i nomi delle funzioni del gestore eventi nel pacchetto, la DLL responsabile dell'implementazione del pacchetto e informazioni sul supporto degli eventi asincroni e della rappresentazione della DLL.

È necessario creare la chiave del Registro di sistema del pacchetto di notifica come sottochiave di

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Notify**

Il nome della chiave è in genere uguale al nome della DLL. Tuttavia, non è obbligatorio. Il nome scelto per il pacchetto non deve essere in conflitto con i nomi di altri pacchetti di notifica installati.

Nella chiave **notifica** del Registro di sistema creare i valori del Registro di sistema seguenti se nel pacchetto è presente una funzione del gestore eventi pertinente.



| Tipo di dati Nome \[ valore\]                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Asincrono** \[ **REG \_ DWORD**\]<br/>    | Indica se il pacchetto può gestire gli eventi in modo asincrono. Se questo valore è impostato su 1, Winlogon chiama le funzioni del pacchetto in un thread separato. In caso contrario, questo non accade.<br/>                                                                                                                                                                                                                                 |
| **DllName** \[ **REG \_ ESPANDERE \_ SZ**\]<br/>    | Nome della DLL che implementa il pacchetto di notifica, ad esempio "Notify.dll".<br/>                                                                                                                                                                                                                                                                                                                          |
| **Rappresentare** \[ **REG \_ DWORD**\]<br/>     | Indica se Winlogon deve rappresentare [](../secgloss/c-gly.md) il contesto di sicurezza dell'utente connesso quando chiama le funzioni del pacchetto di notifica. Se questo valore è impostato su 1, Winlogon usa la rappresentazione. In caso contrario, questo non accade.<br/>                                                                                                                    |
| **Blocco** \[ **REG \_ SZ**\]<br/>               | Nome della funzione che gestisce gli eventi di blocco del desktop, ad esempio "WLEventLock".<br/>                                                                                                                                                                                                                                                                                                                           |
| **Disconnessione** \[ **REG \_ SZ**\]<br/>             | Nome della funzione che gestisce gli eventi di disconnessione, ad esempio "WLEventLogoff".<br/>                                                                                                                                                                                                                                                                                                                               |
| **Accesso** \[ **REG \_ SZ**\]<br/>              | Nome della funzione che gestisce gli eventi di accesso, ad esempio "WLEventLogon".<br/>                                                                                                                                                                                                                                                                                                                                 |
| **Arresto** \[ **REG \_ SZ**\]<br/>           | Nome della funzione che gestisce gli eventi di arresto, ad esempio "WLEventShutdown".<br/>                                                                                                                                                                                                                                                                                                                           |
| **SmartCardLogonNotify** \[ **DWORD**\]<br/> | Indica se Winlogon deve generare una notifica per gli eventi di accesso dalle smart card. Se questo valore è impostato su 1, Winlogon smart card notifiche. In caso contrario, questo non accade.<br/>                                                                                                                                                                                                                     |
| **StartScreenSaver** \[ **REG \_ SZ**\]<br/>   | Nome della funzione che gestisce screen saver eventi di avvio, ad esempio "WLEventStartScreenSaver".<br/>                                                                                                                                                                                                                                                                                                          |
| **StartShell** \[ **REG \_ SZ**\]<br/>         | Nome della funzione che gestisce gli eventi di avvio della shell, ad esempio "WLEventStartShell".<br/> Un evento di avvio della shell si verifica dopo che l'utente ha eseguito l'accesso, ma prima che venga visualizzato il desktop. Si differenzia dall'evento di accesso perché [](../secgloss/c-gly.md) è stato stabilito il contesto di sicurezza dell'utente e sono disponibili risorse come le connessioni di rete.<br/> |
| **Avvio** \[ **REG \_ SZ**\]<br/>            | Nome della funzione che gestisce gli eventi di avvio del sistema, ad esempio "WLEventStartup".<br/>                                                                                                                                                                                                                                                                                                                       |
| **StopScreenSaver** \[ **REG \_ SZ**\]<br/>    | Nome della funzione che gestisce screen saver eventi di arresto, ad esempio" WLEventStopScreenSaver".<br/>                                                                                                                                                                                                                                                                                                            |
| **Sblocca** \[ **REG \_ SZ**\]<br/>             | Nome della funzione che gestisce gli eventi di sblocco del desktop, ad esempio "WLEventUnlock".<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
