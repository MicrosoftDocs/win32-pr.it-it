---
description: Le operazioni di completamento consentono a un'applicazione di specificare come si desidera gestire una sessione quando fattori quali una destinazione occupata impediscono la connessione normale.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Completare una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308310"
---
# <a name="complete-a-session"></a>Completare una sessione

Le operazioni di completamento consentono a un'applicazione di specificare come si desidera gestire una sessione quando fattori quali una destinazione occupata impediscono la connessione normale.

Le [ \_ costanti LINECALLCOMPLMODE](./linecallcomplmode--constants.md) definiscono le possibili opzioni che possono avere un'applicazione, a seconda delle funzionalità del provider di servizi.

Più richieste di completamento delle chiamate potrebbero essere in attesa per un determinato indirizzo in qualsiasi momento. Per identificare le singole richieste, l'implementazione restituisce un [identificatore di completamento](completion-id-ovr.md). L'annullamento di una richiesta di completamento delle chiamate in corso usa anche questo identificatore di completamento della chiamata.

**TAPI 2. x:** Vedere [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).

**TAPI 3. x:** Vedere [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
