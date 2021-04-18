---
description: Il driver UniModel o Universal Modem, TSP (Unimdm. tsp) consente di accedere a quasi tutti i modem standard.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: TSP Unimodem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317033"
---
# <a name="unimodem-tsp"></a>TSP Unimodem

Il driver UniModel o Universal Modem, TSP (Unimdm. tsp) consente di accedere a quasi tutti i modem standard. Supporta modem vocali che consentono lo streaming half-duplex. Sono supportati dall'MSP Wave e il controllo Stream è possibile. (Si noti che UniModel in Windows NT 4,0 o versioni precedenti non supporta modem vocali, quindi il controllo diretto del flusso non è possibile).

Questo TSP supporta un valore del [**tipo di indirizzo**](./lineaddresstype--constants.md) LINEADDRESSTYPE \_ PhoneNumber. Se il programmatore vuole usare le regole di composizione, è necessario usare l'interfaccia [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) di TAPI 3 o la funzione [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) di TAPI 2 per ottenere una stringa di connessione da un numero di telefono in formato canonico.

UniModel TSP viene installato con i sistemi operativi Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 e Windows 95.

 

 
