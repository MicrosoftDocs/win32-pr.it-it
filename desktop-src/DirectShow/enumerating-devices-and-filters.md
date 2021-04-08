---
description: Enumerazione dei dispositivi e dei filtri
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumerazione dei dispositivi e dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876829"
---
# <a name="enumerating-devices-and-filters"></a>Enumerazione dei dispositivi e dei filtri

A volte un'applicazione deve individuare un filtro particolare nel sistema dell'utente. Ad esempio, un'applicazione di acquisizione video potrebbe visualizzare un elenco di dispositivi di acquisizione disponibili. Poiché DirectShow usa un'architettura basata su componenti, non è possibile stabilire in fase di progettazione quali filtri sono installati nel sistema dell'utente. Questa operazione è particolarmente valida per i filtri che rappresentano i dispositivi hardware. DirectShow fornisce due componenti che individuano i filtri registrati:

-   L' [enumeratore di dispositivo di sistema](system-device-enumerator.md) trova i filtri in base alla relativa categoria.
-   Il [mapper del filtro](filter-mapper.md) trova i filtri in base ai criteri di ricerca forniti dall'applicazione.

Gli enumeratori descritti in questa sezione seguono il formato standard usato dalle interfacce di enumerazione COM. Per ulteriori informazioni, vedere l'argomento "IEnumXXXX" in Microsoft Platform Software Development Kit (SDK).

Questa sezione contiene i seguenti argomenti:

-   [Uso di System Device Enumerator](using-the-system-device-enumerator.md)
-   [Uso del mapper dei filtri](using-the-filter-mapper.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività DirectShow di base](basic-directshow-tasks.md)
</dt> </dl>

 

 



