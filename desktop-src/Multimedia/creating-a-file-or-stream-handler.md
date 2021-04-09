---
title: Creazione di un gestore di file o di flussi
description: Creazione di un gestore di file o di flussi
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044579"
---
# <a name="creating-a-file-or-stream-handler"></a>Creazione di un gestore di file o di flussi

In un'applicazione scritta nel linguaggio di programmazione C, un gestore di file o flussi crea in genere una funzione per ogni metodo. L'applicazione accede a queste funzioni tramite una matrice di puntatori a funzione creati dal gestore del flusso. Una struttura **IAVIStreamVtbl** contiene la matrice di puntatori a funzione. Un gestore di flusso può assegnare qualsiasi nome che desideri alle funzioni create per i metodi. La posizione del puntatore a funzione nella struttura implica la corrispondenza della funzione con il metodo. Il primo puntatore a funzione nella struttura, ad esempio, corrisponde al metodo **QueryInterface** . Il gestore del flusso deve fornire tutte le funzioni di un'interfaccia.

 

 




