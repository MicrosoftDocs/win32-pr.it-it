---
description: Ogni identificatore di lingua è composto da un identificatore di lingua principale che indica la lingua e da un identificatore di lingua secondaria che indica il paese o l'area geografica.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Costanti e stringhe degli identificatori di lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67321097d93c5f4224a86a66528f98dacce18312003062665ccc30c1377de70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948748"
---
# <a name="language-identifier-constants-and-strings"></a>Costanti e stringhe degli identificatori di lingua

> [!IMPORTANT]
> Le costanti degli identificatori di lingua sono deprecate e il relativo uso è sconsigliato. È sempre preferibile usare i nomi delle impostazioni locali anziché gli identificatori delle impostazioni locali.

Per [una descrizione degli](language-identifiers.md) identificatori di lingua, vedere l'identificatore di lingua.

Un identificatore primario o secondario può essere definito dall'utente o predefinito. Per gli identificatori di lingua primaria predefiniti con i relativi identificatori di sottolinguaggio validi, vedere [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).

> [!Note]  
> Se non è presente alcun identificatore di sottolinguaggio da usare con un identificatore di lingua principale, l'applicazione deve usare **SUBLANG \_ DEFAULT.** Deve usare **SUBLANG \_ NEUTRAL** per le risorse che sono uguali per tutte le sottolinguaggi di una lingua primaria.

Un identificatore di lingua primaria definito dall'utente ha un valore compreso nell'0x0200 da 0x03ff. Tutti gli altri valori sono riservati per l'uso del sistema operativo.

Un identificatore di sottolinguaggio definito dall'utente ha un valore compreso nell'0x20 da 0x3f. Tutti gli altri valori sono riservati per l'uso del sistema operativo.
