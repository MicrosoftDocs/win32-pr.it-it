---
description: impostazioni locali \_ INvariabili
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306610"
---
# <a name="locale_invariant"></a>impostazioni locali \_ INvariabili

**Windows XP:** Impostazioni locali utilizzate per le funzioni a livello di sistema che richiedono risultati coerenti e indipendenti dalle impostazioni locali. Ad esempio, le impostazioni locali invariabili vengono utilizzate quando un'applicazione confronta le stringhe di caratteri utilizzando la funzione [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e prevede un risultato coerente indipendentemente dalle impostazioni locali dell'utente. Le impostazioni locali invariabili sono simili a quelle per la lingua inglese (Stati Uniti) ma non devono essere utilizzate per visualizzare dati formattati. In genere, un'applicazione non usa l' \_ INvariante delle impostazioni locali perché prevede che i risultati di un'azione dipendano dalle regole che regolano ogni singola impostazione locale. Il valore di impostazioni locali \_ INvariante è 0x007f.

 

 
