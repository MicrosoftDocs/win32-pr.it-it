---
description: Le trasformazioni incorporate vengono archiviate nel file .msi del pacchetto. Ciò garantisce agli utenti che la trasformazione è sempre disponibile quando il pacchetto di installazione è disponibile. In alternativa, le trasformazioni possono essere fornite agli utenti come file mst autonomi.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Trasformazioni incorporate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d7afb2b28599cb9ee2f10c4bc1fb25fbb0939fe68da5e817972eb8fc94236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637463"
---
# <a name="embedded-transforms"></a>Trasformazioni incorporate

Le trasformazioni incorporate vengono archiviate nel file .msi del pacchetto. Ciò garantisce agli utenti che la trasformazione è sempre disponibile quando il pacchetto di installazione è disponibile. In alternativa, le trasformazioni possono essere fornite agli utenti come file mst autonomi.

Per aggiungere una trasformazione incorporata all'elenco delle trasformazioni, aggiungere i due punti (:) prefisso al nome del file. Poiché il programma di installazione può sempre ottenere la trasformazione dall'archiviazione nel file .msi, le trasformazioni incorporate non vengono memorizzate nella cache del computer dell'utente. Le trasformazioni incorporate possono essere usate in combinazione con [trasformazioni protette](secured-transforms.md) o [trasformazioni non protette.](unsecured-transforms.md) Per altre informazioni, vedere [Applicazione di trasformazioni](applying-transforms.md).

 

 



