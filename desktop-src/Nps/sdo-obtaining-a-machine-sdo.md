---
title: Acquisizione di un computer SDO
description: Il primo passaggio nell'uso dell'API SDO consiste nel creare un oggetto computer SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046995"
---
# <a name="obtaining-a-machine-sdo"></a>Acquisizione di un computer SDO

Il primo passaggio nell'uso dell'API SDO consiste nel creare un oggetto computer SDO.

Utilizzare la funzione [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) per ottenere l'identificatore di classe (CLSID) per l'oggetto computer SDO. L'identificatore a livello di codice (ProgID) da usare per l'oggetto è "IAS. SdoMachine".

Una volta ottenuto il CLSID, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con questo CLSID. Specificare [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) come interfaccia per la quale restituire un puntatore.

Vedere [connessione a un Computer SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) per il codice di esempio che illustra come ottenere un SDO del computer.

 

 