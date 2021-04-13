---
title: Inizializzazione di oggetti permanenti
description: Inizializzazione di oggetti permanenti
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399766"
---
# <a name="initializing-persistent-objects"></a>Inizializzazione di oggetti permanenti

Molte delle interfacce di oggetti persistenti, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [Metodo IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))e [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), consentono ai client di inizializzare gli oggetti in uno stato "aggiornato" o "predefinito". Questo stato iniziale è diverso da quello di un oggetto appena creato, che non ha stato.

L'inizializzazione dello stato di un oggetto, anche allo stato predefinito, può essere un'operazione a elevato utilizzo di calcolo o a elevato utilizzo di risorse. Separando la creazione dall'inizializzazione, l'inizializzazione può essere eseguita solo quando è effettivamente necessaria e i client possono evitare di inizializzare gli oggetti allo stato predefinito solo per caricare immediatamente i dati archiviati in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce oggetto permanenti](persistent-object-interfaces.md)
</dt> </dl>

 

 