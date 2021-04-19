---
description: Le chiavi di sessione sono chiavi generate per essere utilizzate in una singola sessione di comunicazione.
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: Chiavi di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317696"
---
# <a name="session-keys"></a>Chiavi di sessione

Le [*chiavi di sessione*](../secgloss/s-gly.md) sono chiavi generate per essere utilizzate in una singola sessione di comunicazione. Le chiavi di sessione vengono modificate di frequente e vengono scartate quando non sono più necessarie. Ad esempio, TLS usa una chiave di sessione separata per ogni connessione e S/MIME usa una chiave di sessione separata per ogni messaggio di posta elettronica. Viene in genere usata una [*chiave simmetrica*](../secgloss/s-gly.md) come chiave della sessione.

Le chiavi della sessione sono volatili. Le applicazioni possono salvare queste chiavi per un uso successivo o per la trasmissione ad altri utenti. Per altre informazioni, vedere [archiviazione delle chiavi crittografiche ed Exchange](cryptographic-key-storage-and-exchange.md).

 

 
