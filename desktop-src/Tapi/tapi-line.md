---
description: La classe del dispositivo TAPI/line è costituita da tutti i dispositivi line. Per accedere a questi dispositivi, usare le funzioni linea TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316023"
---
# <a name="tapiline"></a><span data-ttu-id="658d2-104">TAPI/linea</span><span class="sxs-lookup"><span data-stu-id="658d2-104">tapi/line</span></span>

<span data-ttu-id="658d2-105">La classe del dispositivo TAPI/line è costituita da tutti i dispositivi line.</span><span class="sxs-lookup"><span data-stu-id="658d2-105">The tapi/line device class consists of all line devices.</span></span> <span data-ttu-id="658d2-106">Per accedere a questi dispositivi, usare le funzioni linea TAPI.</span><span class="sxs-lookup"><span data-stu-id="658d2-106">You access these devices using the TAPI line functions.</span></span>

<span data-ttu-id="658d2-107">La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo questo membro aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="658d2-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member.</span></span>

``` syntax
DWORD dwDeviceI;  // line device identifier
```

<span data-ttu-id="658d2-108">Il membro **dwDeviceId** è l'identificatore del dispositivo a linee associato all'handle di linea fornito da [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="658d2-108">The **dwDeviceId** member is the identifier of the line device associated with the line handle given by [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="658d2-109">La funzione [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempie anche una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando **dwStringFormat** su STRINGFORMAT \_ Binary e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="658d2-109">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

<span data-ttu-id="658d2-110">Il membro **adwDeviceIds** è una matrice contenente gli identificatori di dispositivo di tutti i dispositivi a linee associati al dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="658d2-110">The **adwDeviceIds** member is an array containing the device identifiers of all line devices that are associated with the phone device.</span></span> <span data-ttu-id="658d2-111">Se non sono presenti dispositivi linea associati, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) restituisce il \_ valore PHONEERR INVALDEVICECLASS.</span><span class="sxs-lookup"><span data-stu-id="658d2-111">If there are no associated line devices, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) returns the PHONEERR\_INVALDEVICECLASS value.</span></span>

 

 



