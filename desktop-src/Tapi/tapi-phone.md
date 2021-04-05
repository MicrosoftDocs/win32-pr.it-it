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
# <a name="tapiphone"></a>TAPI/Phone

La classe del dispositivo TAPI/Phone è costituita da tutti i dispositivi telefonici. Per accedere a questi dispositivi, usare le funzioni del telefono TAPI.

La funzione [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compila una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

Il membro **dwDeviceId** è l'identificatore del dispositivo telefonico associato all'handle telefonico fornito da [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).

La funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) riempie anche una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando **dwStringFormat** su STRINGFORMAT \_ Binary e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

Il membro **adwDeviceIds** è una matrice contenente gli identificatori di dispositivo di tutti i dispositivi telefonici associati al dispositivo di linea specificato. Se non sono presenti dispositivi telefonici associati, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) restituisce il \_ valore LINEERR INVALDEVICECLASS.

 

 



