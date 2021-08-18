---
description: La classe del dispositivo tapi/phone è costituita da tutti i dispositivi telefonici. È possibile accedere a questi dispositivi usando le funzioni telefoniche TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: tapi/phone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b3238fb2e83d4f6e5e565f40b3ab3b124236ae2c89f879cb284d4a5997f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002719"
---
# <a name="tapiphone"></a>tapi/phone

La classe del dispositivo tapi/phone è costituita da tutti i dispositivi telefonici. È possibile accedere a questi dispositivi usando le funzioni telefoniche TAPI.

La [**funzione phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempie una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando il membro **dwStringFormat** sul valore STRINGFORMAT BINARY e aggiungendo \_ questo membro aggiuntivo:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

Il **membro dwDeviceId** è l'identificatore del dispositivo telefonico associato all'handle del telefono fornito da [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).

La [**funzione lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) riempie anche una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando **dwStringFormat** su STRINGFORMAT BINARY e aggiungendo \_ questo membro aggiuntivo:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

Il **membro adwDeviceIds** è una matrice contenente gli identificatori di dispositivo di tutti i dispositivi telefonici associati al dispositivo linea specificato. Se non sono presenti dispositivi telefonici associati, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) restituisce il valore \_ LINEERR INVALDEVICECLASS.

 

 



