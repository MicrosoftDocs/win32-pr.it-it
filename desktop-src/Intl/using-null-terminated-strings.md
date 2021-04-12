---
description: Quando si usano stringhe con terminazione null, le applicazioni Unicode devono sempre eseguire il cast di zero a TCHAR.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Utilizzo di stringhe con terminazione null
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234191"
---
# <a name="using-null-terminated-strings"></a>Utilizzo di stringhe con terminazione null

Quando si usano stringhe con terminazione null, le applicazioni Unicode devono sempre eseguire il cast di zero a TCHAR. Il codice 0x0000 è il carattere di terminazione della stringa Unicode per una stringa con terminazione null. Un byte null singolo non è sufficiente per questo codice, perché molti caratteri Unicode contengono byte null come valore massimo o basso. Un esempio è la lettera A, per cui il codice carattere è 0x0041.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di caratteri speciali in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



