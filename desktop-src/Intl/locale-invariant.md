---
description: '\_INVARIANTE DELLE IMPOSTAZIONI LOCALI'
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c3a4bddaaa51ca72be9d48f273ac0cbd1727e18e5c821e8ce86acaf0f90ec4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106581"
---
# <a name="locale_invariant"></a>\_INVARIANTE DELLE IMPOSTAZIONI LOCALI

**Windows XP:** Impostazioni locali utilizzate per le funzioni a livello di sistema operativo che richiedono risultati coerenti e indipendenti dalle impostazioni locali. Ad esempio, le impostazioni locali invarianti vengono usate quando un'applicazione confronta stringhe di caratteri usando la funzione [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e prevede un risultato coerente indipendentemente dalle impostazioni locali dell'utente. Le impostazioni delle impostazioni locali invarianti sono simili a quelle per la lingua inglese (Stati Uniti), ma non devono essere usate per visualizzare i dati formattati. In genere, un'applicazione non usa LOCALE INVARIANT perché prevede che i risultati di un'azione dipendono dalle regole che regolano \_ le singole impostazioni locali. Il valore di LOCALE \_ INVARIANT È 0x007f.

 

 
