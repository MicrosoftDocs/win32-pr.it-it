---
description: Vengono descritti i concetti di I/O di base.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Concetti di I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08c8b95df0f5319f9acb62c677b5448ff3f962c8a49eb43c444c391bf139ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533681"
---
# <a name="io-concepts"></a>Concetti di I/O

In questa sezione sono descritti i concetti di I/O seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                               | Descrizione                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Memorizzazione nel buffer dei file](file-buffering.md)<br/>                                     | Vengono descritte le considerazioni per il controllo dell'applicazione del buffer dei file, noto anche come input/output di file senza buffer (I/O).<br/>                                    |
| [Memorizzazione nella cache dei file](file-caching.md)<br/>                                         | Windows memorizza nella cache i dati dei file letti dai dischi e scritti su dischi.<br/>                                                                                   |
| [I/O sincrono e asincrono](synchronous-and-asynchronous-i-o.md)<br/> | Esistono due tipi di sincronizzazione di input/output (I/O): I/O sincrono e I/O asincrono. L'I/O asincrono viene anche definito I/O sovrapposto.<br/> |
| [Annullamento delle operazioni di I/O in sospeso](canceling-pending-i-o-operations.md)<br/> | Consentire agli utenti di annullare richieste di I/O lente o bloccate può migliorare l'usabilità e l'affidabilità dell'applicazione.<br/>                             |
| [I/O con avvisi](alertable-i-o.md)<br/>                                       | L'I/O con avvisi è il metodo con cui i thread dell'applicazione elaborano richieste di I/O asincrone solo quando si trova in uno stato di avviso.<br/>                     |
| [Porte di completamento I/O](i-o-completion-ports.md)<br/>                         | Le porte di completamento I/O forniscono un modello di threading efficiente per l'elaborazione di più richieste di I/O asincrone in un sistema multiprocessore.<br/>                  |



 

 

 




