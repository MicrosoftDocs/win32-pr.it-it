---
title: Effetti della sicurezza sulla ricerca
description: La sicurezza è un filtro implicito durante l'esecuzione di ricerche, l'enumerazione di contenitori o la lettura di proprietà.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- effetti della sicurezza sulla ricerca Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707699"
---
# <a name="effects-of-security-on-searching"></a>Effetti della sicurezza sulla ricerca

La sicurezza è un filtro implicito durante l'esecuzione di ricerche, l'enumerazione di contenitori o la lettura di proprietà.

ADSI non può restituire \_ tali \_ proprietà o \_ \_ errori di questo tipo anche quando l'oggetto esiste se non si dispone dell'accesso per leggere gli attributi sull'oggetto.

Un chiamante, ad esempio, può essere in grado di enumerare gli oggetti figlio in un contenitore perché il chiamante dispone \_ dei diritti di contenuto dell'elenco nel contenitore. Tuttavia, lo stesso chiamante potrebbe non essere in grado di accedere agli oggetti enumerati se il chiamante non dispone dell'accesso in lettura agli oggetti figlio. In questo caso, una query per un oggetto figlio può restituire un oggetto di questo \_ tipo \_ anche se il chiamante ha enumerato correttamente l'oggetto.

Se il chiamante non dispone di diritti sufficienti, è possibile che vengano restituiti i seguenti codici restituiti:

E \_ Ads \_ dominio non valido \_ \_

\_Proprietà Ads \_ E \_ non \_ supportata

\_Proprietà Ads \_ E \_ non \_ trovata

 

 




