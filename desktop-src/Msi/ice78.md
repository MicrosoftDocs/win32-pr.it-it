---
description: ICE78 verifica che la tabella AdvtUISequence non esista o sia vuota. Questa operazione è necessaria perché durante la pubblicità non è consentita alcuna interfaccia utente.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129967"
---
# <a name="ice78"></a>ICE78

ICE78 verifica che la [tabella AdvtUISequence](advtuisequence-table.md) non esista o sia vuota. Questa operazione è necessaria perché durante la pubblicità non è consentita alcuna interfaccia utente.

## <a name="result"></a>Risultato

ICE78 Invia un errore se la tabella AdvtUISequence esiste e non è vuota.

## <a name="example"></a>Esempio

ICE78 segnala l'errore seguente per l'esempio:

L'azione ' action1' è stata trovata nella tabella AdvtUISequence. Non sono consentite interfacce utente durante la pubblicità. La tabella AdvtUISequence deve pertanto essere vuota o non presente.

[Tabella AdvtUISequence](advtuisequence-table.md)(parziale)



| Azione  | Condizione | Sequenza |
|---------|-----------|----------|
| Action1 | true      | 1        |



 

Per correggere l'errore, rimuovere "action1" dalla tabella oppure rimuovere la tabella.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



