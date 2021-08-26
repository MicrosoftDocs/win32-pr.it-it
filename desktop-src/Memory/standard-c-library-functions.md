---
description: Le applicazioni possono usare in modo sicuro le funzionalità di gestione della memoria della libreria di runtime C (malloc, free e così via) e C++ (new, delete e così via).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Funzioni della libreria C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1447a64f00fbd1b4cccf70f7589f267ebba526d66528d7342da68068f81ebfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963211"
---
# <a name="standard-c-library-functions"></a>Funzioni della libreria C standard

Le applicazioni possono usare in modo sicuro le funzionalità di gestione della memoria della libreria di runtime C (**malloc**, **free** e così via) e C++**(new**, **delete** e così via). Le funzioni della libreria di runtime del linguaggio C non hanno i potenziali problemi che hanno sotto i 16 bit Windows. La gestione della memoria non è più un problema perché il sistema è libero di gestire la memoria spostando pagine di memoria fisica senza influire sugli indirizzi virtuali. Analogamente, la distinzione tra puntatori da vicino e da lontano non è più rilevante. Pertanto, è possibile usare le funzioni della libreria C standard per la gestione della memoria. Tuttavia, le funzioni di gestione della memoria forniscono funzionalità non disponibili nella libreria di runtime del linguaggio C.

 

 



