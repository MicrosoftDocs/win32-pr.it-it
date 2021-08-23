---
title: Inizializzazione di oggetti persistenti
description: Inizializzazione di oggetti persistenti
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee98b01c6c9eab28f8f96f98ea1a2980c9eb5d10988c2efbe495a920c98c51e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756181"
---
# <a name="initializing-persistent-objects"></a>Inizializzazione di oggetti persistenti

Diverse interfacce di oggetti persistenti, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))e [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), consentono ai client di inizializzare gli oggetti su uno stato "nuovo" o "predefinito". Questo stato iniziale è diverso da quello di un oggetto appena creato, che non ha stato.

L'inizializzazione dello stato di un oggetto, anche allo stato predefinito, può essere un'operazione a elevato utilizzo di calcolo o a elevato utilizzo di risorse. Separando la creazione dall'inizializzazione, l'inizializzazione può essere eseguita solo quando è effettivamente necessaria e i client possono evitare di inizializzare gli oggetti allo stato predefinito solo per caricare immediatamente i dati archiviati in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce di oggetti persistenti](persistent-object-interfaces.md)
</dt> </dl>

 

 