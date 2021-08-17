---
description: Enumerazione di dispositivi e filtri
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumerazione di dispositivi e filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53f4a36e2bf994cfeab34a49444d104b2213a839bb1fa8bd2aa4d70e0003b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401775"
---
# <a name="enumerating-devices-and-filters"></a>Enumerazione di dispositivi e filtri

In alcuni casi un'applicazione deve individuare un filtro specifico nel sistema dell'utente. Ad esempio, un'applicazione di acquisizione video potrebbe visualizzare un elenco di dispositivi di acquisizione disponibili. Poiché DirectShow usa un'architettura basata su componenti, non è possibile sapere in fase di progettazione quali filtri sono installati nel sistema dell'utente. Ciò vale in particolare per i filtri che rappresentano i dispositivi hardware. DirectShow fornisce due componenti che individuano i filtri registrati:

-   System [Device Enumerator consente di](system-device-enumerator.md) trovare i filtri in base alla categoria.
-   Filter [Mapper trova](filter-mapper.md) i filtri in base ai criteri di ricerca forniti dall'applicazione.

Gli enumeratori descritti in questa sezione seguono il formato standard usato dalle interfacce di enumerazione COM. Per altre informazioni, vedere l'argomento "IEnumXXXX" in Microsoft Platform Software Development Kit (SDK).

Questa sezione contiene i seguenti argomenti:

-   [Utilizzo dell'enumeratore dispositivo di sistema](using-the-system-device-enumerator.md)
-   [Uso del mapper di filtri](using-the-filter-mapper.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività di DirectShow di base](basic-directshow-tasks.md)
</dt> </dl>

 

 



