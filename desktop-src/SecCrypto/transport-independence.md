---
description: I certificati possono essere richiesti e distribuiti tramite qualsiasi meccanismo di trasporto.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Indipendenza del trasporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308648"
---
# <a name="transport-independence"></a>Indipendenza del trasporto

I certificati possono essere richiesti e distribuiti tramite qualsiasi meccanismo di trasporto. Servizi certificati accetta [*richieste di certificati*](../secgloss/c-gly.md) da un richiedente tramite http, DCOM, RPC, file su disco o trasporto personalizzato. Servizi certificati invia certificati al richiedente tramite HTTP, DCOM, RPC, file su disco o trasporto personalizzato.

I trasporti sono supportati dalle applicazioni intermedie e dalle DLL dei moduli di uscita, in genere scritte in C/C++. Le applicazioni intermedie e i moduli di uscita isolano le funzioni di Servizi certificati dalla comunicazione con un trasporto specifico.

 

 
