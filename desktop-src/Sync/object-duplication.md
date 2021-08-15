---
description: La funzione DuplicateHandle crea un handle duplicato che può essere usato da un altro processo specificato.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplicazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927f9d3b60f358623e66a067e75992e71c76ca5fe072a9749c9bbc217bfa2ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886341"
---
# <a name="object-duplication"></a>Duplicazione di oggetti

La [**funzione DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) crea un handle duplicato che può essere usato da un altro processo specificato. Questo metodo di condivisione degli handle di oggetto è più complesso rispetto all'uso di oggetti denominati o ereditarietà. Richiede la comunicazione tra il processo di creazione e il processo in cui l'handle viene duplicato. Le informazioni necessarie (il valore dell'handle e l'identificatore del processo) possono essere comunicate da qualsiasi metodo di comunicazione interprocesso, ad esempio named pipe o memoria condivisa denominata.

 

 
