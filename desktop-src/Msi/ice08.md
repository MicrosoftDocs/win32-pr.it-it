---
description: ICE08 verifica che la tabella Component non contenga GUID duplicati. Ogni componente deve avere un GUID univoco. Se la tabella Component non esiste, non viene eseguita alcuna convalida.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6075b7c895242fe5cfa7608a414643a9e3491787fc59037f8761fa66b18354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745321"
---
# <a name="ice08"></a>ICE08

ICE08 verifica che la tabella [Component non](component-table.md) contenga [GUID duplicati.](guid.md) Ogni componente deve avere un GUID univoco. Se la tabella Component non esiste, non viene eseguita alcuna convalida.

## <a name="result"></a>Risultato

ICE08 invia un messaggio di errore se due o più voci nella colonna ComponentId della tabella Component contengono lo stesso GUID.

## <a name="example"></a>Esempio

Per l'esempio seguente, ICE08 pubblica un messaggio che informa che i componenti Red e Green hanno GUID duplicati.

[Tabella dei componenti](component-table.md) (parziale)



| Componente | Componentid                            |
|-----------|----------------------------------------|
| Red       | {0000000A-0003-0000-0000-624474736554} |
| Blu      | {0000000A-0003-0000-0000-624474736354} |
| Green     | {0000000A-0003-0000-0000-624474736554} |



 

Per correggere l'errore, modificare uno dei GUID duplicati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



