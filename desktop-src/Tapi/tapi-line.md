---
description: La classe del dispositivo tapi/line è costituita da tutti i dispositivi line. È possibile accedere a questi dispositivi usando le funzioni line TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: tapi/line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56478f43d1055d7bf2a382bc84611360675da97e506812a1806df4beca0aeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760733"
---
# <a name="tapiline"></a>tapi/line

La classe del dispositivo tapi/line è costituita da tutti i dispositivi line. È possibile accedere a questi dispositivi usando le funzioni line TAPI.

La [**funzione lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) riempie una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando il membro **dwStringFormat** sul valore STRINGFORMAT BINARY e aggiungendo \_ questo membro aggiuntivo.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

Il **membro dwDeviceId** è l'identificatore del dispositivo di linea associato all'handle di riga specificato da [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

La [**funzione phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempie anche una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando **dwStringFormat** su STRINGFORMAT BINARY e aggiungendo \_ questo membro aggiuntivo:

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

Il **membro adwDeviceIds** è una matrice contenente gli identificatori di dispositivo di tutti i dispositivi line associati al dispositivo telefonico. Se non sono presenti dispositivi line associati, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) restituisce il valore PHONEERR \_ INVALDEVICECLASS.

 

 



