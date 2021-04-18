---
description: Due tipi di terminali Track sono definiti registrazione del terminale di tracking e della riproduzione, che appartengono rispettivamente a e sono gestiti dal terminale di registrazione file e dal terminale di riproduzione file.
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: Rileva terminali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315796"
---
# <a name="track-terminals"></a>Rileva terminali

Sono definiti due tipi di terminali di rilevamento: la registrazione di Track Terminal e playback Track Terminal, che, rispettivamente, appartengono a e sono gestiti dal terminale di registrazione file e dal terminale riproduzione file.

Tutti i terminali di rilevamento espongono le interfacce [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) e [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) . L'interfaccia **ITTerminal** consente la selezione dei terminali di rilevamento nei flussi o nelle chiamate.

> [!Note]  
> I terminali di rilevamento espongono anche un'interfaccia privata, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), che viene usata dal msp. Le applicazioni non devono tentare di accedere a questa interfaccia.

 

 

 
