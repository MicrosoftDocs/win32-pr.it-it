---
description: ICE78 verifica che la tabella AdvtUISequence non esista o sia vuota. Questa operazione è necessaria perché non è consentita alcuna interfaccia utente durante la pubblicità.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39061872b716c9cc05e983d72615bf287683fd9c316df5661c3085e545169f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638121"
---
# <a name="ice78"></a>ICE78

ICE78 verifica che la [tabella AdvtUISequence](advtuisequence-table.md) non esista o sia vuota. Questa operazione è necessaria perché non è consentita alcuna interfaccia utente durante la pubblicità.

## <a name="result"></a>Risultato

ICE78 invia un errore se la tabella AdvtUISequence esiste e non è vuota.

## <a name="example"></a>Esempio

ICE78 segnala l'errore seguente per l'esempio:

Azione 'Action1' trovata nella tabella AdvtUISequence. Durante la pubblicità non è consentita alcuna interfaccia utente. Pertanto, la tabella AdvtUISequence deve essere vuota o non presente.

[Tabella AdvtUISequence](advtuisequence-table.md)(parziale)



| Azione  | Condition | Sequenza |
|---------|-----------|----------|
| Action1 | true      | 1        |



 

Per correggere l'errore, rimuovere "Action1" dalla tabella o rimuovere la tabella.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



