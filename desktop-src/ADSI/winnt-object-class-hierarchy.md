---
title: Gerarchia di classi di oggetti WinNT
description: La gerarchia di classi di oggetti WinNT inizia dall'oggetto spazio dei nomi.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- ADSI provider di servizi WinNT, gerarchia di classi di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515451"
---
# <a name="winnt-object-class-hierarchy"></a>Gerarchia di classi di oggetti WinNT

La gerarchia di classi di oggetti WinNT inizia dall'oggetto spazio dei nomi.



| Object (classe)                   | Descrizione                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Spazio dei nomi<br/>           | Contenitore di oggetti di primo livello.<br/>                                            |
| Dominio<br/>              | Dominio Windows NT.<br/>                                                 |
| User<br/>                | Account utente.<br/>                                                          |
| Group<br/>               | Account di gruppo per la gestione dei diritti di accesso.<br/>                              |
| UserGroupCollection<br/> | Set di gruppi di utenti che implementa [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/>  |
| GroupCollection<br/>     | Un set di altri gruppi che implementano [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/> |
| Computer<br/>            | Server o workstation Windows NT 4,0.<br/>                                  |
| PrintJob<br/>            | Processo di stampa nella coda di stampa.<br/>                                          |
| PrintJobsCollection<br/> | Set di processi di stampa.<br/>                                                   |
| PrintQueue<br/>          | Coda di stampa sullo spooler di una stampante.<br/>                                      |
| Servizio<br/>             | Applicazione in esecuzione come servizio.<br/>                                      |
| FileService<br/>         | Servizi che accedono a file system.<br/>                                        |
| FileShare<br/>           | Punto di condivisione file.<br/>                                                      |
| Risorsa<br/>            | Risorsa nel servizio.<br/>                                             |
| Sessione<br/>             | Connessione al servizio file attiva.<br/>                                     |
| User<br/>                | Account utente locale.<br/>                                                    |
| Group<br/>               | Gruppo locale.<br/>                                                           |
| UserCollection<br/>      | Raccolta di utenti locali.<br/>                                             |
| GroupCollection<br/>     | Raccolta di gruppi locali.<br/>                                            |
| SCHEMA<br/>              | Contenitore dello schema WinNT.<br/>                                                |
| Classe<br/>               | Definizione della classe dello schema.<br/>                                               |
| Proprietà<br/>            | Definizione dell'attributo dello schema.<br/>                                           |
| Sintassi<br/>              | Sintassi di una proprietà.<br/>                                                  |



 

 

 





