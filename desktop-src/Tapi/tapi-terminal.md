---
description: La classe del dispositivo TAPI/terminal è costituita dai dispositivi telefonici associati a ogni terminale su una linea o dal terminale in ogni riga associata a un dispositivo telefonico. Per accedere a questi dispositivi, è possibile usare il dispositivo linea TAPI o le funzioni del dispositivo telefonico.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/terminale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315263"
---
# <a name="tapiterminal"></a><span data-ttu-id="f624b-104">TAPI/terminale</span><span class="sxs-lookup"><span data-stu-id="f624b-104">tapi/terminal</span></span>

<span data-ttu-id="f624b-105">La classe del dispositivo TAPI/terminal è costituita dai dispositivi telefonici associati a ogni terminale su una linea o dal terminale in ogni riga associata a un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="f624b-105">The tapi/terminal device class consists of the phone devices associated with each terminal on a line or the terminal on each line associated with a phone device.</span></span> <span data-ttu-id="f624b-106">Per accedere a questi dispositivi, è possibile usare il [dispositivo linea](line-device-functions.md) TAPI o le [funzioni del dispositivo telefonico](phone-device-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f624b-106">You access these devices by using the TAPI [line device](line-device-functions.md) or [phone device functions](phone-device-functions.md).</span></span>

<span data-ttu-id="f624b-107">La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="f624b-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

<span data-ttu-id="f624b-108">Il membro **adwDeviceId** è una matrice di identificatori di dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="f624b-108">The **adwDeviceId** member is an array of phone device identifiers.</span></span> <span data-ttu-id="f624b-109">È presente un elemento di matrice per ogni terminale specificato dal membro **dwNumTerminals** nella struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo di linea specificato.</span><span class="sxs-lookup"><span data-stu-id="f624b-109">There is one array element for each terminal specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the given line device.</span></span> <span data-ttu-id="f624b-110">Ogni elemento specifica l'identificatore del dispositivo telefonico associato al terminale corrispondente sulla riga.</span><span class="sxs-lookup"><span data-stu-id="f624b-110">Each element specifies the identifier of the phone device associated with the corresponding terminal on the line.</span></span> <span data-ttu-id="f624b-111">Se non è presente alcun dispositivo telefonico associato a un terminale, l'elemento viene impostato su-1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="f624b-111">If there is no phone device associated with a terminal, the element is set to –1 (0xFFFFFFFF).</span></span>

<span data-ttu-id="f624b-112">La funzione [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="f624b-112">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

<span data-ttu-id="f624b-113">Il membro **adwTerminalID** è una matrice di identificatori di terminale.</span><span class="sxs-lookup"><span data-stu-id="f624b-113">The **adwTerminalID** member is an array of terminal identifiers.</span></span> <span data-ttu-id="f624b-114">È presente un elemento di matrice per ogni identificatore di dispositivo linea specificato dalla funzione [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="f624b-114">There is one array element for each line device identifier specified by the [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) function.</span></span> <span data-ttu-id="f624b-115">Ogni elemento della matrice contiene l'identificatore del terminale associato al dispositivo telefonico per il dispositivo di linea specificato.</span><span class="sxs-lookup"><span data-stu-id="f624b-115">Each array element contains the terminal identifier associated with the phone device for the given line device.</span></span> <span data-ttu-id="f624b-116">Se non è presente alcun dispositivo telefonico, l'elemento viene impostato su-1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="f624b-116">If there is no phone device, the element is set to –1 (0xFFFFFFFF).</span></span> <span data-ttu-id="f624b-117">Gli identificatori di terminale hanno un valore compreso tra zero e uno inferiore al numero specificato dal membro **dwNumTerminals** nella struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="f624b-117">The terminal identifiers range in value from zero to one less than the number specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>

 

 



