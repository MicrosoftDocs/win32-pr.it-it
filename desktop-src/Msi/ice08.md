---
description: ICE08 verifica che la tabella dei componenti non contenga GUID duplicati. Ogni componente deve avere un GUID univoco. Se la tabella dei componenti non esiste, non viene eseguita alcuna convalida.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314243"
---
# <a name="ice08"></a>ICE08

ICE08 verifica che la [tabella dei componenti](component-table.md) non contenga [GUID](guid.md)duplicati. Ogni componente deve avere un GUID univoco. Se la tabella dei componenti non esiste, non viene eseguita alcuna convalida.

## <a name="result"></a>Risultato

ICE08 Invia un messaggio di errore se due o più voci nella colonna ComponentId della tabella dei componenti contengono lo stesso GUID.

## <a name="example"></a>Esempio

Per l'esempio seguente, ICE08 Invia un messaggio che informa che i componenti rosso e verde presentano GUID duplicati.

[Tabella componenti](component-table.md) (parziale)



| Componente | ComponentId                            |
|-----------|----------------------------------------|
| Red       | {0000000A-0003-0000-0000-624474736554} |
| Blu      | {0000000A-0003-0000-0000-624474736354} |
| Green     | {0000000A-0003-0000-0000-624474736554} |



 

Per correggere l'errore, modificare uno dei GUID duplicati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



