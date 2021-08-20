---
title: Caratteristiche di prestazioni
description: Una chiamata all'implementazione del file composto COM dell'interfaccia IPropertySetStorage per creare un set di proprietà determina la creazione di un flusso o di una memoria tramite una chiamata a IStorage CreateStream o IStorage CreateStorage.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac11200b021cae1ea1d60438b57530f0dbc8c02ea3d26b5622ab859a99224aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960831"
---
# <a name="performance-characteristics"></a>Caratteristiche di prestazioni

Una chiamata all'implementazione del file composto COM dell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare un set di proprietà determina la creazione di un flusso o di una memoria tramite una chiamata a [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage). Un set di proprietà predefinito viene creato in memoria, ma non scaricato su disco. Quando è presente una chiamata a [**IPropertyStorage::WriteMultiple,**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)funziona all'interno del buffer.

Quando viene aperto un set di proprietà, viene usato [IStorage::OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [IStorage::OpenStorage.](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) L'intero flusso del set di proprietà viene letto nella memoria contigua. [**Le operazioni IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) vengono quindi eseguite leggendo il buffer di memoria. Pertanto, il primo accesso è costoso in termini di tempo (a causa delle operazioni di lettura del disco), ma gli accessi successivi sono molto efficienti. Le operazioni di scrittura possono essere leggermente più costose perché le operazioni SetSize nel flusso sottostante possono essere necessarie per garantire che lo spazio su disco sia disponibile se vengono aggiunti dati.

Non viene garantito se [**IPropertyStorage::WriteMultiple scarica**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) gli aggiornamenti. In generale, il client deve presupporre che **IPropertyStorage::WriteMultiple anteponga** solo l'oggetto nel buffer di memoria. Per scaricare i dati, è necessario chiamare [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) o [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (ultima versione).

Ciò significa che [**WriteMultiple può avere**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) esito positivo, ma i dati non vengono effettivamente scritti in modo permanente.

> [!Note]  
> Questa dimensione del flusso del set di proprietà non può superare i 256.000 byte.

 

 

 