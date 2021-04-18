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
# <a name="unimodem-tsp"></a><span data-ttu-id="81528-103">TSP Unimodem</span><span class="sxs-lookup"><span data-stu-id="81528-103">Unimodem TSP</span></span>

<span data-ttu-id="81528-104">Il driver UniModel o Universal Modem, TSP (Unimdm. tsp) consente di accedere a quasi tutti i modem standard.</span><span class="sxs-lookup"><span data-stu-id="81528-104">The Unimodem, or Universal Modem Driver, TSP (Unimdm.tsp) provides access to nearly all standard modems.</span></span> <span data-ttu-id="81528-105">Supporta modem vocali che consentono lo streaming half-duplex.</span><span class="sxs-lookup"><span data-stu-id="81528-105">It supports voice modems that allow half-duplex streaming.</span></span> <span data-ttu-id="81528-106">Sono supportati dall'MSP Wave e il controllo Stream è possibile.</span><span class="sxs-lookup"><span data-stu-id="81528-106">They are supported by the Wave MSP and stream control is possible.</span></span> <span data-ttu-id="81528-107">(Si noti che UniModel in Windows NT 4,0 o versioni precedenti non supporta modem vocali, quindi il controllo diretto del flusso non è possibile).</span><span class="sxs-lookup"><span data-stu-id="81528-107">(Note that Unimodem on Windows NT 4.0 or earlier does not support voice modems, so direct stream control is not possible.)</span></span>

<span data-ttu-id="81528-108">Questo TSP supporta un valore del [**tipo di indirizzo**](./lineaddresstype--constants.md) LINEADDRESSTYPE \_ PhoneNumber.</span><span class="sxs-lookup"><span data-stu-id="81528-108">This TSP supports an [**address type**](./lineaddresstype--constants.md) value of LINEADDRESSTYPE\_PHONENUMBER.</span></span> <span data-ttu-id="81528-109">Se il programmatore vuole usare le regole di composizione, è necessario usare l'interfaccia [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) di TAPI 3 o la funzione [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) di TAPI 2 per ottenere una stringa di connessione da un numero di telefono in formato canonico.</span><span class="sxs-lookup"><span data-stu-id="81528-109">If the programmer wants to use the dialing rules, the TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) interface or the TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) function must be used to obtain a dialable string from a phone number in canonical format.</span></span>

<span data-ttu-id="81528-110">UniModel TSP viene installato con i sistemi operativi Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="81528-110">The Unimodem TSP is installed with Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98, and Windows 95.</span></span>

 

 
