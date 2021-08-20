---
description: Un file di tipo sparse influisce sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva allocata di spazio su disco.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: File di tipo sparse e quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e78e9d35e557585f17df6c4672a04b2997792f95b0fca63d2e6a2345a7a8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015079"
---
# <a name="sparse-files-and-disk-quotas"></a>File di tipo sparse e quote disco

Un file di tipo sparse influisce sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva allocata di spazio su disco. Ciò significa che la creazione di un file da 50 MB con tutti zero byte consuma 50 MB della quota dell'utente. Ciò significa che quando l'utente scrive dati nel file di tipo sparse, non deve preoccuparsi di superare il limite di quota rigida, perché è già stato addebitato per lo spazio. Gli amministratori di sistema non devono contare sulle dimensioni di un file di tipo sparse rimanenti. Pertanto, non devono concedere agli utenti limiti di quota rigidi che superano lo spazio fisico disponibile, nonostante l'uso di file di tipo sparse.

 

 



