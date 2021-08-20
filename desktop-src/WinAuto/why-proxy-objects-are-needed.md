---
title: Perché sono necessari oggetti proxy
description: Con gli oggetti accessibili, quando un client imposta una funzione hook nel contesto, la DLL in cui viene implementata la funzione hook del client viene caricata nello spazio degli indirizzi del server.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7038a43bf238d9baebee81e13cd82d904dc1b8a4c9ed7fb0c1576f42cbdfdfb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860991"
---
# <a name="why-proxy-objects-are-needed"></a>Perché sono necessari oggetti proxy

Con gli oggetti accessibili, quando un client imposta una funzione [hook nel](in-context-and-out-of-context-hook-functions.md)contesto , la DLL in cui viene implementata la funzione hook del client viene caricata nello spazio degli indirizzi del server. In questo caso, quando il client chiama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) dall'interno della funzione hook, il puntatore a interfaccia restituito punta direttamente al codice nello spazio degli indirizzi del server. Quando il client chiama una proprietà dell'interfaccia usando questo puntatore, la libreria Component Object Model (COM) non è coinvolta nel marshalling o nell'annullamento del marshalling e non è in grado di rilevare se un oggetto viene eliminato. Pertanto, il server deve rilevare questa situazione e restituire un codice di errore al client.

 

 




