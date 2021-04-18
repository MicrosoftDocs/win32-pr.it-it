---
title: Attributi ACF di gestione degli errori e delle eccezioni
description: Usare gli attributi seguenti per la gestione degli errori.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- MIDL, attributi, errori e gestione delle eccezioni di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299790"
---
# <a name="error-and-exception-handling-acf-attributes"></a>Attributi ACF di gestione degli errori e delle eccezioni

Usare gli attributi seguenti per la gestione degli errori.



| Attributo                                                                | Utilizzo                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| stato di errore [**\_ dello stato di comunicazione**](comm-status.md)[**\_**](fault-status.md) | Consentire all'applicazione client di gestire le eccezioni normalmente causando la restituzione delle comunicazioni e degli errori del server al client come valori dei parametri. L'applicazione client può quindi chiamare la funzione della fase di esecuzione RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) per inoltrare un messaggio di errore all'utente. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Importazione di file e librerie dei tipi](importing-files-and-type-libraries.md)
</dt> </dl>

 

 