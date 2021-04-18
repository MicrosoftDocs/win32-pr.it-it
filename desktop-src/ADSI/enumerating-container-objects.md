---
title: Enumerazione degli oggetti contenitore
description: Per convenzione, tutti gli elementi in un'enumerazione in ADSI devono avere lo stesso tipo di dati di automazione. Ad esempio, un'enumerazione non deve restituire alcuni elementi come VARIANT di tipo VT \_ I4 e altri come Variant di tipo VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297685"
---
# <a name="enumerating-container-objects"></a>Enumerazione degli oggetti contenitore

Per convenzione, tutti gli elementi in un'enumerazione in ADSI devono avere lo stesso tipo di dati di automazione. Ad esempio, un'enumerazione non deve restituire alcuni elementi come **Variant** di tipo **VT \_ I4** e altri come **Variant** di tipo **VT \_ BSTR**.

Per enumerare un elenco di elementi gestiti da un oggetto, un client richiede la creazione di un oggetto di enumerazione per il tipo specifico di informazioni elencate. In ADSI il client può elencare gli oggetti in oggetti spazio dei nomi, oggetti contenitore generici, oggetti raccolta, oggetti membro o oggetti dello schema. ADSI fornisce un filtro che può essere impostato e modificato per limitare le corrispondenze in qualsiasi enumerazione tramite la proprietà [**IADsContainer. Filter**](iadscontainer-property-methods.md) . Esempi di implementazioni degli oggetti enumeratore sono disponibili nel codice del componente provider di esempio per gli oggetti contenitore ADs seguenti.



| Tipo di oggetto         | codice         |
|---------------------|--------------|
| Contenitore generico   | cenumobj. cpp |
| Contenitore spazio dei nomi | cenumns. cpp  |
| Contenitore dello schema    | cenumsch. cpp |



 

Per informazioni sul lato client, vedere [raccolte e gruppi](collections-and-groups.md).

 

 




