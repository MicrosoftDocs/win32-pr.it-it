---
title: Tipi di dati delle funzioni e valori restituiti
description: Tipi di dati delle funzioni e valori restituiti
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955390"
---
# <a name="function-data-types-and-return-values"></a>Tipi di dati delle funzioni e valori restituiti

Le funzioni e le macro AVIFile utilizzano gestori di file e flussi implementati con la tecnologia OLE. Il tipo di dati standard di una funzione OLE è **STDAPI** e la funzione restituisce un valore **HRESULT** (zero in caso di esito positivo o errore). Se una funzione restituisce un valore diverso da **HRESULT**, il tipo del prototipo della funzione presenta una sintassi leggermente diversa che incorpora il tipo di valore restituito tra parentesi che seguono "STDAPI \_ ". Ad esempio, una funzione che restituisce un valore di dati **Long** USA **STDAPI \_ (Long)** nell'istruzione Prototype.

 

 




