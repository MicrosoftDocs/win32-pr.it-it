---
description: Le funzioni seguenti sono i punti di ingresso per le DLL di esperti e per le chiamate dal sistema operativo e Network Monitor.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funzioni di esportazione DLL di esperti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966482"
---
# <a name="expert-dll-export-functions"></a>Funzioni di esportazione DLL di esperti

Le funzioni seguenti sono i punti di ingresso per le DLL di esperti e per le chiamate dal sistema operativo e Network Monitor.



| Funzione                                   | Descrizione                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Esperto DllMain**](dllmain-expert.md)   | Indica che la DLL di esperti è stata caricata o scaricata. Quando un processo carica o Scarica la DLL, il sistema operativo chiama la funzione [**DllMain**](/windows/desktop/Dlls/dllmain) . |
| [**Registra esperto**](register-expert.md) | Determina le informazioni di base sull'esperto all'interno della DLL. Network Monitor chiama la funzione **Register** .                                                           |
| [**Configurare**](configure.md)             | Configura l'esperto all'interno della DLL. Network Monitor chiama la funzione [**Configure**](configure.md) .                                                                 |
| [**Correre**](run.md)                         | Avvia l'esperto all'interno della DLL. Network Monitor chiama la funzione [**Run**](run.md) .                                                                                 |



 

Network Monitor fornisce anche strutture, enumerazioni e funzioni di supporto che l'esperto può chiamare.



| Per informazioni su                                      | Vedere                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni helper che possono essere chiamate da esperti e analizzatori | [Funzioni comuni di esperti e parser](expert-and-parser-common-functions.md) |
| Funzioni di supporto chiamate solo da esperti           | [Funzioni di esperti](expert-functions.md)                                     |
| Strutture utilizzate dalle funzioni di esperti               | [Strutture di esperti](expert-structures.md)                                   |
| Enumerazioni utilizzate da funzioni e strutture di esperti       | [Enumerazioni di esperti](expert-enumerations.md)                               |



 

 

 
