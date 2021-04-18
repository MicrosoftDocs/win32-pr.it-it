---
description: In TAPI sono disponibili numerose funzioni per la modifica degli handle di chiamata, per determinare la relazione tra linee, chiamate e indirizzi e così via.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Manipolazione dell'handle di chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309963"
---
# <a name="call-handle-manipulation"></a>Manipolazione dell'handle di chiamata

In TAPI sono disponibili numerose funzioni per la modifica degli handle di chiamata, per determinare la relazione tra linee, chiamate e indirizzi e così via. La maggior parte di questa funzionalità è implementata rigorosamente all'interno di TAPI senza riferimento al provider di servizi, ad eccezione di [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid). Questa funzione recupera l'identificatore dell'indirizzo di una chiamata esistente all'interno della relativa riga. I provider di servizi che modellano una linea come gruppo di identificatori di indirizzi possono scegliere un indirizzo imprevedibile per una nuova chiamata in ingresso o in uscita. Questa funzione assegna a TAPI informazioni sufficienti per implementare l'operazione [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) quando viene richiamata con l' \_ opzione LINECALLSELECT Address.

 

 
