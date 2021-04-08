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
# <a name="obtaining-a-machine-sdo"></a><span data-ttu-id="c6d57-103">Acquisizione di un computer SDO</span><span class="sxs-lookup"><span data-stu-id="c6d57-103">Obtaining a Machine SDO</span></span>

<span data-ttu-id="c6d57-104">Il primo passaggio nell'uso dell'API SDO consiste nel creare un oggetto computer SDO.</span><span class="sxs-lookup"><span data-stu-id="c6d57-104">The first step in using the SDO API is to create an SDO machine object.</span></span>

<span data-ttu-id="c6d57-105">Utilizzare la funzione [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) per ottenere l'identificatore di classe (CLSID) per l'oggetto computer SDO.</span><span class="sxs-lookup"><span data-stu-id="c6d57-105">Use the [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) function to obtain the class identifier (CLSID) for the SDO machine object.</span></span> <span data-ttu-id="c6d57-106">L'identificatore a livello di codice (ProgID) da usare per l'oggetto è "IAS. SdoMachine".</span><span class="sxs-lookup"><span data-stu-id="c6d57-106">The programmatic identifier (ProgID) to use for the object is "IAS.SdoMachine".</span></span>

<span data-ttu-id="c6d57-107">Una volta ottenuto il CLSID, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con questo CLSID.</span><span class="sxs-lookup"><span data-stu-id="c6d57-107">Once you have the CLSID, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with this CLSID.</span></span> <span data-ttu-id="c6d57-108">Specificare [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) come interfaccia per la quale restituire un puntatore.</span><span class="sxs-lookup"><span data-stu-id="c6d57-108">Specify [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) as the interface for which to return a pointer.</span></span>

<span data-ttu-id="c6d57-109">Vedere [connessione a un Computer SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) per il codice di esempio che illustra come ottenere un SDO del computer.</span><span class="sxs-lookup"><span data-stu-id="c6d57-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to obtain a machine SDO.</span></span>

 

 