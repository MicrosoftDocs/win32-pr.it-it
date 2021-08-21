---
description: Un'applicazione TAPI deve chiamare un'operazione di inizializzazione, che richiede una serie di azioni da TAPI e dai provider di servizi che configurano l'ambiente di comunicazione per l'applicazione.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inizializzazione primaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae187692f1eb64546398a273bc823ab93f622b6a0472848c31f9d94b9ecd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060589"
---
# <a name="primary-initialization"></a>Inizializzazione primaria

Un'applicazione TAPI deve chiamare un'operazione di inizializzazione, che richiede una serie di azioni da TAPI e dai provider di servizi che configurano l'ambiente di comunicazione per l'applicazione.

-   L'inizializzazione è sincrona e non restituisce un valore finché l'operazione non è stata completata o non è riuscita.
-   Se TAPISRV non è già in esecuzione, viene avviato da TAPI.
-   TAPI configura una connessione al processo TAPISRV.
-   TAPISVR carica i provider di servizi specificati nel Registro di sistema e richiede di inizializzare i dispositivi supportati.

**TAPI 2.x:** Le applicazioni eseguono l'inizializzazione chiamando [**lineInitializeEx.**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)

**TAPI 3.x:** Le applicazioni [**chiamano ITTAPI::Initialize.**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)

 

 
