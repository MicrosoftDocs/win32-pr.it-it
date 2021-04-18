---
description: L'API Location definisce i tipi di enumerazione seguenti.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Strutture e tipi di enumerazione (API Location)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314798"
---
# <a name="structures-and-enumeration-types-location-api"></a>Strutture e tipi di enumerazione (API Location)

\[L'API del percorso Win32 è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) . \]

L'API Location definisce i tipi di enumerazione seguenti.



| Enumerazione                                                                       | Descrizione                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_ \_ accuratezza posizione desiderata**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))                  | Definisce i possibili tipi di accuratezza desiderati.                         |
| [**\_stato rapporto \_ percorso**](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | Definisce lo stato possibile per i nuovi report di un tipo di report specifico. |



 

## <a name="location-constants-from-the-sensor-api"></a>Costanti di posizione dall'API del sensore

L'API del sensore definisce anche le chiavi delle proprietà relative alla posizione e le costanti. È possibile utilizzare le chiavi di proprietà definite in sensors. h per recuperare i dati del percorso da un report chiamando [**ILocationReport:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).

 

 
