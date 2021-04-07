---
description: La funzione DuplicateHandle crea un handle duplicato che può essere usato da un altro processo specificato.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplicazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057866"
---
# <a name="object-duplication"></a>Duplicazione di oggetti

La funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) crea un handle duplicato che può essere usato da un altro processo specificato. Questo metodo di condivisione degli handle di oggetto è più complesso rispetto all'utilizzo di oggetti o ereditarietà denominati. Richiede la comunicazione tra il processo di creazione e il processo in cui l'handle viene duplicato. Le informazioni necessarie (il valore dell'handle e l'identificatore del processo) possono essere comunicate da uno qualsiasi dei metodi di comunicazione interprocesso, ad esempio Named Pipes o Shared Memory.

 

 
