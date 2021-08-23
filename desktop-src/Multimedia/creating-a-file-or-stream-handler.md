---
title: Creazione di un gestore di file o di flusso
description: Creazione di un gestore di file o di flusso
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6732c572e390f3401f6e0472659bec7c522189b357b04d8ef7def20a7d9519b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785791"
---
# <a name="creating-a-file-or-stream-handler"></a>Creazione di un gestore di file o di flusso

In un'applicazione scritta nel linguaggio di programmazione C, un gestore di file o di flusso crea in genere una funzione per ogni metodo. L'applicazione accede a queste funzioni tramite una matrice di puntatori a funzione creati dal gestore del flusso. Una **struttura IAVIStreamVtbl** contiene la matrice di puntatori a funzione. Un gestore di flusso può assegnare qualsiasi nome che vuole funzioni che crea per i metodi. La posizione del puntatore a funzione nella struttura implica la corrispondenza della funzione con il metodo . Ad esempio, il primo puntatore a funzione nella struttura corrisponde al **metodo QueryInterface.** Il gestore di flusso deve fornire tutte le funzioni di un'interfaccia.

 

 




