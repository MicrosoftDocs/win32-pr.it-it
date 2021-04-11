---
description: Un file sparse influiscono sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva di spazio su disco allocata.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: File sparse e quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129758"
---
# <a name="sparse-files-and-disk-quotas"></a>File sparse e quote disco

Un file sparse influiscono sulle quote utente in base alle dimensioni nominali del file, non alla quantità effettiva di spazio su disco allocata. Ovvero la creazione di un file di 50 MB con tutti i byte zero utilizza 50 MB della quota di tale utente. Ciò significa che quando l'utente scrive i dati nel file sparse, non è necessario preoccuparsi del superamento del limite di quota hardware perché è già stato addebitato per lo spazio. Gli amministratori di sistema non devono contare sulle dimensioni di un file sparse che rimane ridotto. Non devono quindi concedere ai propri utenti limiti di quota rigidi che superano lo spazio fisico disponibile, nonostante l'uso di file sparse.

 

 



