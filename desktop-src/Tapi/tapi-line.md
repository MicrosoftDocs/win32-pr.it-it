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
# <a name="tapiline"></a>TAPI/linea

La classe del dispositivo TAPI/line è costituita da tutti i dispositivi line. Per accedere a questi dispositivi, usare le funzioni linea TAPI.

La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo questo membro aggiuntivo.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

Il membro **dwDeviceId** è l'identificatore del dispositivo a linee associato all'handle di linea fornito da [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

La funzione [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempie anche una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando **dwStringFormat** su STRINGFORMAT \_ Binary e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

Il membro **adwDeviceIds** è una matrice contenente gli identificatori di dispositivo di tutti i dispositivi a linee associati al dispositivo telefonico. Se non sono presenti dispositivi linea associati, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) restituisce il \_ valore PHONEERR INVALDEVICECLASS.

 

 



