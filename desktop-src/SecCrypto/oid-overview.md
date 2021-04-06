---
description: L'estendibilità viene eseguita fornendo per l'utilizzo di nuovi identificatori di oggetto (OID), nuovi tipi di codifica e nuove dll.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Panoramica di OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883610"
---
# <a name="oid-overview"></a>Panoramica di OID

L'estendibilità viene eseguita fornendo per l'utilizzo di nuovi [*identificatori di oggetto*](../secgloss/o-gly.md) (OID), nuovi tipi di codifica e nuove dll.

CryptoAPI OID può assumere uno dei seguenti formati:

-   Stringa numerica, ad esempio "1.2.3.500.88"
-   Stringa alfanumerica, ad esempio *funzione*
-   Costante con un valore minore o uguale a 0xFFFF. Queste costanti sono spesso associate a un nome tramite l'utilizzo di un'istruzione **\# define** in un file di intestazione.

Le funzioni estendibili accettano gli argomenti di tipo OID e di codifica. Queste funzioni consentono di eseguire ricerche nel registro di sistema per trovare una DLL associata all'OID e gli argomenti di tipo di codifica passati alla funzione. Se viene rilevata una DLL per il tipo di codifica OID, viene caricata la DLL e viene chiamata la relativa funzione. La figura seguente illustra questo flusso per la funzione [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :

![flusso OID](images/oidflow.png)

Ciò consente di estendere la funzionalità della CryptoAPI in modo da richiedere l'estensione. L'uso di questa metodologia impone agli sviluppatori della nuova funzionalità di scrivere tutto il codice necessario per tale funzionalità. Per codificare una nuova struttura di dati, ad esempio, la funzione nella DLL deve eseguire l'intero processo di codifica.

 

 
