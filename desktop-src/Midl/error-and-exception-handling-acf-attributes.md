---
title: Attributi ACF di gestione degli errori e delle eccezioni
description: Usare gli attributi seguenti per la gestione degli errori.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF MIDL, attributi, gestione degli errori e delle eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f780145854a463da9a983c7dccbb24b01c2eca16437bf1254f93ec34def5395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384427"
---
# <a name="error-and-exception-handling-acf-attributes"></a>Attributi ACF di gestione degli errori e delle eccezioni

Usare gli attributi seguenti per la gestione degli errori.



| Attributo                                                                | Utilizzo                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**stato comm \_ status**](comm-status.md)[**fault \_ status**](fault-status.md) | Consentire all'applicazione client di gestire correttamente le eccezioni causando la generazione di errori di comunicazione e server al client come valori di parametro. L'applicazione client può quindi chiamare la funzione di run-time RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) per inoltrare un messaggio di errore all'utente. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Importazione di file e librerie dei tipi](importing-files-and-type-libraries.md)
</dt> </dl>

 

 