---
description: Le applicazioni possono utilizzare in modo sicuro le funzionalità di gestione della memoria della libreria di runtime C (malloc, free e così via) e C++ (nuovo, DELETE e così via).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Funzioni della libreria C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308334"
---
# <a name="standard-c-library-functions"></a>Funzioni della libreria C standard

Le applicazioni possono utilizzare in modo sicuro le funzionalità di gestione della memoria della libreria di runtime C (**malloc**, **Free** e così via) e C++ (**nuovo**, **Delete** e così via). Le funzioni della libreria di runtime C non presentano i potenziali problemi in Windows a 16 bit. La gestione della memoria non è più un problema perché il sistema è libero di gestire la memoria spostando le pagine della memoria fisica senza influire sugli indirizzi virtuali. Analogamente, la distinzione tra i puntatori near e lontano non è più pertinente. Pertanto, è possibile utilizzare le funzioni della libreria C standard per la gestione della memoria. Tuttavia, le funzioni di gestione della memoria forniscono funzionalità non disponibili nella libreria di runtime del linguaggio C.

 

 



