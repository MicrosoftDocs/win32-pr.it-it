---
description: Un'applicazione TAPI deve chiamare un'operazione di inizializzazione, che richiede una serie di azioni da TAPI e i provider di servizi che configurano l'ambiente di comunicazione per l'applicazione.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inizializzazione primaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316039"
---
# <a name="primary-initialization"></a>Inizializzazione primaria

Un'applicazione TAPI deve chiamare un'operazione di inizializzazione, che richiede una serie di azioni da TAPI e i provider di servizi che configurano l'ambiente di comunicazione per l'applicazione.

-   L'inizializzazione è sincrona e non restituisce alcun risultato fino a quando l'operazione non viene completata o non è riuscita.
-   Se TAPISRV non è già in esecuzione, TAPI lo avvia.
-   TAPI configura una connessione al processo TAPISRV.
-   TAPISVR carica i provider di servizi specificati nel registro di sistema e chiede di inizializzare i dispositivi supportati.

**TAPI 2. x:** Le applicazioni eseguono l'inizializzazione chiamando [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

**TAPI 3. x:** Le applicazioni chiamano [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).

 

 
