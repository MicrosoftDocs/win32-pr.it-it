---
title: Connessione al computer SDO
description: Con il puntatore di interfaccia restituito da CoCreateInstance, chiamare il metodo di associazione ISdoMachine.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963158"
---
# <a name="attaching-to-the-sdo-computer"></a>Connessione al computer SDO

Con il puntatore di interfaccia restituito da [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), chiamare il metodo [**ISdoMachine:: alconnessione**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) . Passare **null** come parametro al metodo di **connessione** . Il valore **null** **specifica che associa associare l'** oggetto computer al computer locale. La connessione a un computer remoto non è supportata.

Per determinare se il computer locale è già collegato, chiamare il metodo [**ISdoMachine:: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .

Vedere [connessione a un computer SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) per il codice di esempio che illustra come connettersi al computer locale.

 

 