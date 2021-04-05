---
description: La classe del dispositivo TAPI/Phone è costituita da tutti i dispositivi telefonici. Per accedere a questi dispositivi, usare le funzioni del telefono TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/Phone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967982"
---
# <a name="tapiphone"></a><span data-ttu-id="df5b2-104">TAPI/Phone</span><span class="sxs-lookup"><span data-stu-id="df5b2-104">tapi/phone</span></span>

<span data-ttu-id="df5b2-105">La classe del dispositivo TAPI/Phone è costituita da tutti i dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="df5b2-105">The tapi/phone device class consists of all phone devices.</span></span> <span data-ttu-id="df5b2-106">Per accedere a questi dispositivi, usare le funzioni del telefono TAPI.</span><span class="sxs-lookup"><span data-stu-id="df5b2-106">You access these devices by using the TAPI phone functions.</span></span>

<span data-ttu-id="df5b2-107">La funzione [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="df5b2-107">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

<span data-ttu-id="df5b2-108">Il membro **dwDeviceId** è l'identificatore del dispositivo telefonico associato all'handle telefonico fornito da [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="df5b2-108">The **dwDeviceId** member is the identifier of the phone device associated with the phone handle given by [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span>

<span data-ttu-id="df5b2-109">La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) riempie anche una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando **dwStringFormat** su STRINGFORMAT \_ Binary e aggiungendo il membro aggiuntivo seguente:</span><span class="sxs-lookup"><span data-stu-id="df5b2-109">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

<span data-ttu-id="df5b2-110">Il membro **adwDeviceIds** è una matrice contenente gli identificatori di dispositivo di tutti i dispositivi telefonici associati al dispositivo di linea specificato.</span><span class="sxs-lookup"><span data-stu-id="df5b2-110">The **adwDeviceIds** member is an array containing the device identifiers of all phone devices that are associated with the given line device.</span></span> <span data-ttu-id="df5b2-111">Se non sono presenti dispositivi telefonici associati, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) restituisce il \_ valore LINEERR INVALDEVICECLASS.</span><span class="sxs-lookup"><span data-stu-id="df5b2-111">If there are no associated phone devices, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) returns the LINEERR\_INVALDEVICECLASS value.</span></span>

 

 



