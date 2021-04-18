---
description: Se si usano più riconoscitori, è possibile usare la raccolta Recognizers per elencare i riconoscitori disponibili e consentire a un utente di effettuare una selezione tra di essi.
ms.assetid: 1b89def0-3491-42da-9138-5280002e447a
title: Uso della raccolta Recognizers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d38625b3c6d4b8ed2475393ba45ae97b5bdc47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306707"
---
# <a name="using-the-recognizers-collection"></a>Uso della raccolta Recognizers

Se si usano più riconoscitori, è possibile usare la raccolta [**Recognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) per elencare i riconoscitori disponibili e consentire a un utente di effettuare una selezione tra di essi. Una raccolta **Recognizers** verifica la presenza di riconoscitori installati, esegue una query sugli attributi degli oggetti [**Recognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) e archivia i risultati. Le applicazioni possono utilizzare la raccolta **Recognizers** per visualizzare un elenco di riconoscitori disponibili senza caricare ogni DLL del riconoscitore.

> [!Note]  
> La raccolta [**Recognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) usa il registro di sistema per verificare sia i riconoscitori Microsoft che i riconoscitori di terze parti.

 

La tabella seguente mostra i valori degli identificatori di lingua supportati da ogni riconoscimento Microsoft.

> [!Note]  
> Nessun identificatore di lingua associato al riconoscitore di movimento Microsoft.

 



| Nome riconoscimento                                                      | ID lingua primaria, ID lingua (in ordine supportato)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Riconoscimento movimento Microsoft<br/>                              | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Riconoscimento grafia Microsoft English (Regno Unito)<br/> | LANG \_ English, sottolang \_ English \_ UK<br/> LANG \_ English, Eire ( \_ lingua inglese) \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Riconoscimento grafia Microsoft inglese (Stati Uniti)<br/>  | LANG \_ English, sottolang \_ English \_ US<br/> LANG \_ English, sottolang \_ English \_ aus<br/> LANG \_ English, sottolang \_ English \_ Belize<br/> LANG \_ English, sottolang \_ English \_ can<br/> LANG \_ English, sottolang \_ English \_ Caribbean<br/> LANG \_ English, sottolang \_ English \_ Jamaica<br/> LANG \_ English, sottolang \_ English \_ NZ<br/> LANG \_ English, sottolang \_ English \_ Philippines<br/> LANG \_ English, sottolang \_ English \_ Sudafrica \_<br/> LANG \_ English, SUBLANG \_ English \_ Trinidad<br/> LANG \_ English, sottolang \_ English \_ Zimbabwe<br/> LANG \_ English, SUBLANG \_ neutral<br/> |
| Riconoscimento grafia francese Microsoft<br/>                   | LANG \_ francese, SUBLANG \_ francese<br/> LANG \_ francese, SUBLANG \_ francese \_ belga<br/> LANG \_ francese, SUBLANG \_ francese \_ canadese<br/> LANG \_ francese, SUBLANG \_ francese \_ Luxembourg<br/> LANG \_ francese, SUBLANG \_ francese \_ Monaco<br/> LANG \_ francese, SUBLANG \_ francese \_ svizzero<br/> LANG \_ francese, SUBLANG \_ neutro<br/>                                                                                                                                                                                                                                                                                     |
| Riconoscimento grafia tedesco Microsoft<br/>                   | LANG \_ tedesco, SUBLANG \_ tedesco<br/> LANG \_ tedesco, SUBLANG \_ tedesco \_ austriaco<br/> LANG \_ tedesco, SUBLANG \_ tedesco \_ Liechtenstein<br/> LANG \_ German, SUBLANG \_ German \_ Luxembourg<br/> LANG \_ tedesco, SUBLANG \_ tedesco \_ svizzero<br/> LANG \_ tedesco, SUBLANG \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                |
| Riconoscimento grafia Microsoft spagnolo<br/>                  | LANG \_ spagnolo, SUBLANG \_ spagnolo<br/> LANG \_ spagnolo, SUBLANG \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Riconoscimento grafia giapponese Microsoft<br/>                 | LANG \_ japanese, SUBLANG \_ neutral<br/> LANG \_ japanese, valore predefinito di SUBlang \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Riconoscimento grafia Microsoft Korean<br/>                   | LANG \_ coreano, sottolang \_ neutro<br/> LANG \_ coreano, valore predefinito di SUBlang \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Riconoscimento grafia Microsoft cinese (semplificato)<br/>     | LANG \_ cinese, \_ lingua cinese \_ semplificata<br/> LANG \_ cinese, SUBLANG \_ Chinese \_ Singapore<br/> LANG \_ cinese, SUBLANG \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Riconoscimento grafia Microsoft cinese (tradizionale)<br/>    | LANG \_ cinese, SUBLANG \_ cinese \_ tradizionale<br/> LANG \_ cinese, SUBLANG \_ Chinese \_ Hongkong<br/> LANG \_ cinese, SUBLANG \_ Chinese \_ Macau<br/> LANG \_ cinese, SUBLANG \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

Per altre informazioni sugli identificatori di lingua, vedere [costanti e stringhe degli identificatori di lingua](../intl/language-identifier-constants-and-strings.md).

 

 
