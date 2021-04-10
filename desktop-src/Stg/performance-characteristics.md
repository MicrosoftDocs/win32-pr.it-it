---
title: Caratteristiche di prestazioni
description: Una chiamata all'implementazione del file composto COM dell'interfaccia IPropertySetStorage per creare un set di proprietà comporta la creazione di un flusso o di una risorsa di archiviazione tramite una chiamata a IStorage CreateStream o IStorage CreateStorage.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8597862602a367ed93a3d6e5e0bcac76035c337a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963233"
---
# <a name="performance-characteristics"></a>Caratteristiche di prestazioni

Una chiamata all'implementazione del file composto COM dell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare un set di proprietà comporta la creazione di un flusso o di una risorsa di archiviazione tramite una chiamata a [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage). Un set di proprietà predefinito viene creato in memoria, ma non viene scaricato su disco. Quando viene eseguita una chiamata a [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple), questo opera all'interno del buffer.

Quando viene aperto un set di proprietà, viene usato [IStorage:: OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [IStorage:: OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) . L'intero flusso del set di proprietà viene letto nella memoria contigua. Le operazioni [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) quindi operano leggendo il buffer di memoria. Pertanto, il primo accesso è dispendioso in termini di tempo (a causa delle letture su disco), ma gli accessi successivi sono molto efficienti. Le scritture possono essere leggermente più onerose perché è possibile che le operazioni di ridimensionamento nel flusso sottostante garantiscano la disponibilità di spazio su disco in caso di aggiunta di dati.

Non viene garantita alcuna garanzia in merito al fatto che [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) effettui lo scaricamento degli aggiornamenti. In generale, il client deve presupporre che **IPropertyStorage:: WriteMultiple** aggiorni solo il buffer in memoria. Per svuotare i dati, è necessario chiamare [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) o [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (ultima versione).

Questo progetto significa che [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) può avere esito positivo, ma i dati non vengono effettivamente scritti in modo permanente.

> [!Note]  
> Questa dimensione del flusso del set di proprietà non può superare 256K byte.

 

 

 