---
description: Il driver unimodem o universal modem, TSP (Unimdm.tsp) fornisce l'accesso a quasi tutti i modem standard.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4562ad7692c288a963db27b6859fa5c472d8ff80017e2726c277fbf9d24452be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011901"
---
# <a name="unimodem-tsp"></a>Unimodem TSP

Il driver unimodem o universal modem, TSP (Unimdm.tsp) fornisce l'accesso a quasi tutti i modem standard. Supporta i modem vocali che consentono lo streaming half-duplex. Sono supportati da Wave MSP ed è possibile controllare il flusso. Si noti che Unimodem Windows NT 4.0 o versioni precedenti non supporta i modem vocali, pertanto il controllo diretto del flusso non è possibile.

Questo provider di servizi di rete supporta un [**valore del tipo**](./lineaddresstype--constants.md) di indirizzo LINEADDRESSTYPE \_ PHONENUMBER. Se il programmatore vuole usare le regole di composizione, è necessario usare l'interfaccia TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) o la funzione TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) per ottenere una stringa dialable da un numero di telefono in formato canonico.

Il provider di servizi di configurazione Unimodem viene installato con sistemi operativi Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 e Windows 95.

 

 
