---
description: ICE89 verifica che il valore nella colonna Progid Parent della tabella ProgId sia una chiave esterna valida nella colonna \_ ProgId della tabella ProgId. Ogni elemento padre ProgId deve avere un record nella tabella ProgId.
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c40845c5a6d26147b8435b46e1a31f62e985468cbfe1986b6ba79950763d9c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828861"
---
# <a name="ice89"></a>ICE89

ICE89 verifica che il valore nella colonna Progid Parent della tabella ProgId sia una chiave esterna valida nella colonna \_ ProgId della tabella ProgId. [](progid-table.md) Ogni elemento padre ProgId deve avere un record nella tabella ProgId.

## <a name="result"></a>Risultato

ICE89 pubblica gli errori seguenti.



| Errore ICE89                                                           | Descrizione                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| Il ProgId \_ padre ' \[ 1 ' nella tabella \] ProgId non è un ProgId valido. | È stato specificato un elemento padre ProgId non elencato nella tabella ProgId. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



