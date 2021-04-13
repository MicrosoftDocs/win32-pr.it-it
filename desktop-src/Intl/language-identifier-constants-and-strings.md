---
description: Ogni identificatore di lingua è costituito da un identificatore di lingua principale che indica la lingua e un identificatore di lingua secondaria che indica il paese/area geografica.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Costanti e stringhe degli identificatori di lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346041"
---
# <a name="language-identifier-constants-and-strings"></a>Costanti e stringhe degli identificatori di lingua

> [!IMPORTANT]
> Le costanti identificatore della lingua sono deprecate e il loro utilizzo è sconsigliato. L'uso di nomi delle impostazioni locali invece degli identificatori delle impostazioni locali è sempre preferibile.

Per una descrizione degli identificatori di lingua, vedere [identificatore](language-identifiers.md) della lingua.

Un identificatore primario o sublingua può essere definito dall'utente o predefinito. Per gli identificatori di lingua primaria predefiniti con i relativi identificatori di sottolingua validi, vedere [[MS-LCID]: informazioni di riferimento sull'identificatore del codice lingua (LCID) di Windows](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).

> [!Note]  
> Se non è disponibile alcun identificatore di lingua per l'uso con un identificatore di lingua principale, l'applicazione deve usare l' **\_ impostazione predefinita di SUBLANG**. Per le risorse identiche per tutte le sottolingue di una lingua primaria, è necessario usare la sottolingua **\_ neutra** .

Un identificatore della lingua primaria definito dall'utente ha un valore compreso nell'intervallo tra 0x0200 e 0x03ff. Tutti gli altri valori sono riservati per l'utilizzo del sistema operativo.

Un identificatore di lingua inglese definito dall'utente ha un valore compreso nell'intervallo tra 0x20 e 0x3F. Tutti gli altri valori sono riservati per l'utilizzo del sistema operativo.
