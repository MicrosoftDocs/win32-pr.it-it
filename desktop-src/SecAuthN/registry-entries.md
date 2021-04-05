---
description: Illustra le voci del registro di sistema per gli eventi Winlogon.
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: Voci del registro di sistema (autenticazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d50b413d99d2bc31a7af4e8e101ab27e51a8892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881433"
---
# <a name="registry-entries-authentication"></a>Voci del registro di sistema (autenticazione)

Per consentire al pacchetto di ricevere le notifiche degli eventi da [*Winlogon*](../secgloss/w-gly.md), è necessario fornire il nome del pacchetto, i nomi delle funzioni del gestore eventi nel pacchetto, la dll responsabile dell'implementazione del pacchetto e informazioni sul fatto che la DLL supporti gli eventi asincroni e la rappresentazione.

È necessario creare la chiave del registro di sistema del pacchetto di notifica come sottochiave di

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **notifica**

Il nome della chiave è in genere uguale al nome della DLL. Tuttavia, questa operazione non è obbligatoria. Il nome scelto per il pacchetto non deve essere in conflitto con i nomi degli altri pacchetti di notifiche installati.

Nella chiave del registro di sistema **Notify** creare i valori del registro di sistema seguenti se nel pacchetto è presente una funzione del gestore eventi pertinente.



| Tipo di \[ dati nome valore\]                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Operazione **asincrona** \[ **Reg \_ DWORD**\]<br/>    | Indica se il pacchetto è in grado di gestire gli eventi in modo asincrono. Se questo valore è impostato su 1, Winlogon chiama le funzioni del pacchetto in un thread separato. In caso contrario, questo non accade.<br/>                                                                                                                                                                                                                                 |
| **Dllname** \[ **Reg \_ Espandi \_ SZ**\]<br/>    | Nome della DLL che implementa il pacchetto di notifica, ad esempio: "Notify.dll".<br/>                                                                                                                                                                                                                                                                                                                          |
| **Rappresenta** \[ **Reg \_ DWORD**\]<br/>     | Indica se Winlogon deve rappresentare il [*contesto*](../secgloss/c-gly.md) di sicurezza dell'utente connesso quando chiama le funzioni del pacchetto di notifica. Se questo valore è impostato su 1, Winlogon utilizza la rappresentazione. In caso contrario, questo non accade.<br/>                                                                                                                    |
| **Blocca** \[ **Reg \_ SZ**\]<br/>               | Nome della funzione che gestisce gli eventi di blocco desktop, ad esempio: "WLEventLock".<br/>                                                                                                                                                                                                                                                                                                                           |
| **Disconnessione** \[ **Reg \_ SZ**\]<br/>             | Nome della funzione che gestisce gli eventi di disconnessione, ad esempio: "WLEventLogoff".<br/>                                                                                                                                                                                                                                                                                                                               |
| **Accesso** \[ **Reg \_ SZ**\]<br/>              | Nome della funzione che gestisce gli eventi di accesso, ad esempio: "WLEventLogon".<br/>                                                                                                                                                                                                                                                                                                                                 |
| **Arresta** \[ **Reg \_ SZ**\]<br/>           | Nome della funzione che gestisce gli eventi di arresto, ad esempio: "WLEventShutdown".<br/>                                                                                                                                                                                                                                                                                                                           |
| **SmartCardLogonNotify** \[ **DWORD**\]<br/> | Indica se Winlogon deve generare una notifica per gli eventi di accesso dalle smart card. Se questo valore è impostato su 1, Winlogon consente le notifiche di smart card. In caso contrario, questo non accade.<br/>                                                                                                                                                                                                                     |
| **StartScreenSaver** \[ **Reg \_ SZ**\]<br/>   | Nome della funzione che gestisce gli eventi di avvio screen saver, ad esempio: "WLEventStartScreenSaver".<br/>                                                                                                                                                                                                                                                                                                          |
| **StartShell** \[ **Reg \_ SZ**\]<br/>         | Nome della funzione che gestisce gli eventi di avvio della shell, ad esempio: "WLEventStartShell".<br/> Un evento di avvio della shell si verifica dopo che l'utente ha effettuato l'accesso ma prima che venga visualizzato il desktop. Si differenzia dall'evento LOGON in quanto è stato stabilito il [*contesto*](../secgloss/c-gly.md) di sicurezza dell'utente e sono disponibili risorse quali le connessioni di rete.<br/> |
| **Avvio** \[ di **Reg \_ SZ**\]<br/>            | Nome della funzione che gestisce gli eventi di avvio del sistema, ad esempio: "WLEventStartup".<br/>                                                                                                                                                                                                                                                                                                                       |
| **StopScreenSaver** \[ **Reg \_ SZ**\]<br/>    | Nome della funzione che gestisce gli eventi di arresto screen saver, ad esempio: "WLEventStopScreenSaver".<br/>                                                                                                                                                                                                                                                                                                            |
| **Sblocca** \[ **Reg \_ SZ**\]<br/>             | Nome della funzione che gestisce gli eventi di sblocco del desktop, ad esempio: "WLEventUnlock".<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
