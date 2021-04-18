---
description: Il programma di installazione Application Programming Interface (API) fornisce un set di funzioni che l'applicazione di installazione può chiamare per eseguire operazioni di installazione. Queste funzioni di configurazione funzionano con i file INF di Windows per fornire le funzionalità di configurazione seguenti.
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: Panoramica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32b99c6079fdb61fd6bfd0033ffccb9ebb7b922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313279"
---
# <a name="overview"></a>Panoramica

Il programma di installazione Application Programming Interface (API) fornisce un set di funzioni che l'applicazione di installazione può chiamare per eseguire operazioni di installazione. Queste funzioni di configurazione funzionano con i file INF di Windows per fornire le funzionalità di configurazione seguenti.



| Per informazioni su                       | Vedere                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accodamento di file                               | [Code di file](file-queues.md)                                                                                                                                              |
| Installazione dei file                            | [Code di file](file-queues.md)<br/> [Configurare le applicazioni](setup-applications.md)<br/> [Creazione di applicazioni di installazione](creating-setup-applications.md)<br/> |
| Gestione degli errori e richiesta di supporto     | [Richieste di dischi e gestione degli errori](disk-prompting-and-error-handling.md)                                                                                                  |
| Aggiornamento delle voci del registro di sistema                   | [Configurare le applicazioni](setup-applications.md)                                                                                                                                |
| Registrazione dei file installati                     | [Log file](file-log.md)                                                                                                                                                    |
| Archiviazione dei percorsi di origine usati più di recente | [Elenco origine MRU](mru-source-list.md)                                                                                                                                      |



 

Per la maggior parte delle funzioni di configurazione sono disponibili versioni Unicode e ANSI. I file di testo Unicode devono contenere l'indicatore dell'ordine dei byte 0xFEFF standard per consentire alle funzioni di installazione di identificare il file come testo Unicode.

Sebbene l'API di installazione supporti la richiesta di nuove finestre di dialogo per la gestione degli errori e dei supporti, le funzioni di installazione non forniscono funzionalità della procedura guidata o un'interfaccia utente generica.

Gli sviluppatori devono considerare se possono usare [Windows Installer](/windows/desktop/Msi/windows-installer-portal) per installare le applicazioni anziché l'API di installazione. Windows Installer riduce il costo totale di proprietà (TCO) per i clienti, consentendo loro di installare e configurare in modo efficiente i prodotti e le applicazioni. Il programma di installazione può inoltre fornire al prodotto nuove funzionalità per annunciare le funzionalità senza installarle, installare i prodotti su richiesta e aggiungere personalizzazioni utente.

 

