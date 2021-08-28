---
title: Recupero di un SDO del computer
description: Il primo passaggio per l'uso dell'API SDO consiste nel creare un oggetto computer SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9217333440235d5adac544e00420f8564513510908a89a1da7494cf7ba2772ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128601"
---
# <a name="obtaining-a-machine-sdo"></a>Recupero di un SDO del computer

Il primo passaggio per l'uso dell'API SDO consiste nel creare un oggetto computer SDO.

Usare la [**funzione CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) per ottenere l'identificatore di classe (CLSID) per l'oggetto computer SDO. L'identificatore programmatico (ProgID) da usare per l'oggetto è "IAS. SdoMachine".

Dopo aver creato il CLSID, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con questo CLSID. Specificare [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) come interfaccia per cui restituire un puntatore.

Vedere [Collegamento a un computer SDO-Enabled per](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) il codice di esempio che illustra come ottenere un SDO del computer.

 

 