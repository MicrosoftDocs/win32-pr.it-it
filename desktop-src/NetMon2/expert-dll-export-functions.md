---
description: Le funzioni seguenti sono i punti di ingresso per le DLL esperte e per le chiamate dal sistema operativo e Network Monitor.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funzioni di esportazione di DLL esperte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327b36990ac377595b31b55ebc0ed57157fd8d411f690aff3378293f35e39e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911131"
---
# <a name="expert-dll-export-functions"></a>Funzioni di esportazione di DLL esperte

Le funzioni seguenti sono i punti di ingresso per le DLL esperte e per le chiamate dal sistema operativo e Network Monitor.



| Funzione                                   | Descrizione                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DllMain Expert**](dllmain-expert.md)   | Indica che la DLL esperta è stata caricata o scaricata. Quando un processo carica o scarica la DLL, il sistema operativo chiama la [**funzione DllMain.**](/windows/desktop/Dlls/dllmain) |
| [**Registrare Un esperto**](register-expert.md) | Determina le informazioni di base sull'esperto all'interno della DLL. Network Monitor chiama la **funzione Register.**                                                           |
| [**Configurare**](configure.md)             | Configura l'esperto all'interno della DLL. Network Monitor chiama la [**funzione Configure.**](configure.md)                                                                 |
| [**Esegui**](run.md)                         | Avvia l'esperto all'interno della DLL. Network Monitor chiama la [**funzione Run.**](run.md)                                                                                 |



 

Network Monitor fornisce anche strutture, enumerazioni e funzioni helper che l'esperto può chiamare.



| Per informazioni su                                      | Vedere                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni helper che possono essere chiamate da esperti e parser | [Funzioni comuni di Expert e Parser](expert-and-parser-common-functions.md) |
| Funzioni helper chiamate solo da esperti           | [Funzioni esperte](expert-functions.md)                                     |
| Strutture usate dalle funzioni esperte               | [Strutture di esperti](expert-structures.md)                                   |
| Enumerazioni usate da strutture e funzioni esperte       | [Enumerazioni di esperti](expert-enumerations.md)                               |



 

 

 
