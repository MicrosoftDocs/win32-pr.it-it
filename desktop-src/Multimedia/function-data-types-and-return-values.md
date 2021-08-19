---
title: Tipi di dati delle funzioni e valori restituiti
description: Tipi di dati delle funzioni e valori restituiti
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d85ed42a0751147a1a6a61a078ac0899ce0b5756467005fd02ec72d6190096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988316"
---
# <a name="function-data-types-and-return-values"></a>Tipi di dati delle funzioni e valori restituiti

Le funzioni e le macro AVIFile usano gestori di file e flussi implementati con la tecnologia OLE. Il tipo di dati standard di una funzione OLE è **STDAPI** e la funzione restituisce un valore **HRESULT** (zero per l'esito positivo o un errore in caso contrario). Se una funzione restituisce un valore diverso da **HRESULT,** il tipo del prototipo della funzione ha una sintassi leggermente diversa che incorpora il tipo di valore restituito tra parentesi dopo "STDAPI". \_ Ad esempio, una funzione che restituisce un **valore di** dati LONG usa **STDAPI \_ (LONG) nell'istruzione** prototype.

 

 




