---
description: Quando si usano stringhe con terminazione Null, le applicazioni Unicode devono sempre eseguire il cast di zero a TCHAR.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Uso di stringhe con terminazione Null
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a5f27048bde2af75eca28626a562473ceffcc66f3f2f23509beca4fba06ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631781"
---
# <a name="using-null-terminated-strings"></a>Uso di stringhe con terminazione Null

Quando si usano stringhe con terminazione Null, le applicazioni Unicode devono sempre eseguire il cast di zero a TCHAR. Il codice 0x0000 è il terminatore di stringa Unicode per una stringa con terminazione Null. Un singolo byte Null non è sufficiente per questo codice, perché molti caratteri Unicode contengono byte Null come byte alto o basso. Un esempio è la lettera A, per cui il codice carattere è 0x0041.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di caratteri speciali in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



