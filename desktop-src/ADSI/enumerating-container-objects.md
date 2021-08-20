---
title: Enumerazione di oggetti contenitore
description: Per convenzione, tutti gli elementi di un'enumerazione in ADSI devono essere dello stesso tipo di dati di Automazione. Ad esempio, un'enumerazione non deve restituire alcuni elementi come VARIANT di tipo VT I4 e altri come VARIANT di \_ tipo VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff6bb6d05a34ce6434531338a877d2dd4aaee2cd4df0b38c81b50b7f56db4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428560"
---
# <a name="enumerating-container-objects"></a>Enumerazione di oggetti contenitore

Per convenzione, tutti gli elementi di un'enumerazione in ADSI devono essere dello stesso tipo di dati di Automazione. Ad esempio, un'enumerazione non deve restituire alcuni elementi come **VARIANT** di tipo **VT \_ I4** e altri come **VARIANT** di **tipo VT \_ BSTR**.

Per enumerare un elenco di elementi mantenuti da un oggetto , un client richiede la creazione di un oggetto di enumerazione per il tipo specifico di informazioni elencate. In ADSI, il client può elencare gli oggetti negli oggetti dello spazio dei nomi, negli oggetti contenitore generici, negli oggetti raccolta, negli oggetti membro o negli oggetti dello schema. ADSI fornisce un filtro che può essere impostato e modificato per limitare le corrispondenze in qualsiasi enumerazione tramite la [**proprietà IADsContainer.Filter.**](iadscontainer-property-methods.md) Esempi di implementazioni di oggetti enumeratore sono disponibili nel codice del componente del provider di esempio per gli oggetti contenitore ADs seguenti.



| Tipo di oggetto         | codice         |
|---------------------|--------------|
| Contenitore generico   | cenumobj.cpp |
| Contenitore dello spazio dei nomi | cenumns.cpp  |
| Contenitore dello schema    | cenumsch.cpp |



 

Per informazioni sul lato client, vedere [Raccolte e gruppi](collections-and-groups.md).

 

 




