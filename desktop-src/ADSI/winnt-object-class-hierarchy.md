---
title: Gerarchia di classi di oggetti WinNT
description: La gerarchia della classe di oggetti WinNT inizia dall'oggetto Namespace.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- Provider di servizi WinNT ADSI, gerarchia di classi di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e893839393ad3b9aaa42557d90f9bf279ab0625e1225ab41f2d1a3c7e7980a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589761"
---
# <a name="winnt-object-class-hierarchy"></a>Gerarchia di classi di oggetti WinNT

La gerarchia della classe di oggetti WinNT inizia dall'oggetto Namespace.



| Object (classe)                   | Descrizione                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Spazio dei nomi<br/>           | Contenitore di oggetti di primo livello.<br/>                                            |
| Dominio<br/>              | Dominio Windows NT locale.<br/>                                                 |
| Utente<br/>                | Account utente.<br/>                                                          |
| Group<br/>               | Account di gruppo per la gestione dei diritti di accesso.<br/>                              |
| UserGroupCollection<br/> | Set di gruppi di utenti che [**implementano IADsMembers.**](/windows/desktop/api/Iads/nn-iads-iadsmembers)<br/>  |
| Groupcollection<br/>     | Set di altri gruppi che implementano [**IADsMembers.**](/windows/desktop/api/Iads/nn-iads-iadsmembers)<br/> |
| Computer<br/>            | Windows NT server o workstation 4.0.<br/>                                  |
| Printjob<br/>            | Processo di stampa nella coda di stampa.<br/>                                          |
| PrintJobsCollection<br/> | Set di processi di stampa.<br/>                                                   |
| PrintQueue<br/>          | Coda di stampa su uno spooler di stampa.<br/>                                      |
| Servizio<br/>             | Applicazione in esecuzione come servizio.<br/>                                      |
| FileService<br/>         | Servizi che accedono file system.<br/>                                        |
| FileShare<br/>           | Punto di condivisione file.<br/>                                                      |
| Risorsa<br/>            | Risorsa nel servizio.<br/>                                             |
| Sessione<br/>             | Una connessione al servizio file attiva.<br/>                                     |
| Utente<br/>                | Account utente locale.<br/>                                                    |
| Group<br/>               | Gruppo locale.<br/>                                                           |
| UserCollection<br/>      | Raccolta di utenti locali.<br/>                                             |
| Groupcollection<br/>     | Raccolta di gruppi locali.<br/>                                            |
| Schema<br/>              | Contenitore dello schema WinNT.<br/>                                                |
| Classe<br/>               | Definizione della classe dello schema.<br/>                                               |
| Proprietà<br/>            | Definizione dell'attributo dello schema.<br/>                                           |
| Sintassi<br/>              | Sintassi di una proprietà.<br/>                                                  |



 

 

 





