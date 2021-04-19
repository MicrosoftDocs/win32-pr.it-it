---
description: Descrive I concetti di base di I/O.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Concetti di I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317781"
---
# <a name="io-concepts"></a>Concetti di I/O

In questa sezione vengono descritti i concetti di I/O seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                               | Descrizione                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Buffering dei file](file-buffering.md)<br/>                                     | Vengono descritte le considerazioni per il controllo dell'applicazione del buffering dei file, noto anche come input/output (I/O) file non memorizzato nel buffer.<br/>                                    |
| [Memorizzazione nella cache dei file](file-caching.md)<br/>                                         | Windows memorizza nella cache i dati del file letti dai dischi e scritti nei dischi.<br/>                                                                                   |
| [I/O sincrono e asincrono](synchronous-and-asynchronous-i-o.md)<br/> | Esistono due tipi di sincronizzazione di input/output (I/O): I/o sincrono e I/O asincrono. L'I/O asincrono è noto anche come I/O sovrapposto.<br/> |
| [Annullamento di operazioni di I/O in sospeso](canceling-pending-i-o-operations.md)<br/> | Consentire agli utenti di annullare le richieste di I/O lente o bloccate può migliorare l'usabilità e l'affidabilità dell'applicazione.<br/>                             |
| [I/O Alertable](alertable-i-o.md)<br/>                                       | L'I/O Alertable è il metodo mediante il quale i thread dell'applicazione elaborano le richieste I/O asincrone solo quando sono in uno stato di avviso.<br/>                     |
| [Porte di completamento I/O](i-o-completion-ports.md)<br/>                         | Le porte di completamento i/O forniscono un modello di threading efficiente per l'elaborazione di più richieste di I/O asincrone in un sistema multiprocessore.<br/>                  |



 

 

 




