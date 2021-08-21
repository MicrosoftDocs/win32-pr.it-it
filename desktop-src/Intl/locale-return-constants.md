---
description: Costanti \_ LOCALE RETURN \*
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: costanti LOCALE_RETURN*
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58714897333f69b058588f9050b9bb52ed29c37d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466028"
---
# <a name="locale_return-constants"></a>Costanti \_ LOCALE RETURN \*

In questo argomento vengono definite le costanti \_ LOCALE RETURN usate da \* NLS.




| valore | Significato | 
|-------|---------|
| LOCALE_RETURN_GENITIVE_NAMES | <strong>Windows 7 e versioni successive:</strong> Recuperare i nomi dei mesi, ovvero i nomi usati quando i nomi dei mesi vengono combinati con altri elementi. Ad esempio, in Avana l'equivalente di gennaio viene scritto "Січень" quando il mese viene denominato da solo. Tuttavia, quando il nome del mese viene usato in combinazione, ad esempio, in una data come il 5 gennaio 2003, viene usata la forma genitiva del nome. Per l'esempio Disempliede, il nome del mese descrittivo viene visualizzato come "5 січня 2003". L'elenco dei nomi dei mesi genitivi inizia con gennaio ed è delimitato da punto e virgola. Se non è presente alcun tredicesimo mese, usare un punto e virgola al suo posto alla fine dell'elenco.<blockquote>[!Note]<br />I nomi dei mesi genitivi non esistono in tutte le lingue.</blockquote><br /><br /> | 
| LOCALE_RETURN_NUMBER | <strong>Windows Me/98, Windows NT 4.0 e versioni successive:</strong> Recuperare un numero. Questa costante fa <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>in modo che GetLocaleInfo</strong></a> o <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recuperi un valore come numero anziché come stringa. Il buffer che riceve il valore deve essere almeno la lunghezza di un valore DWORD. Questa costante può essere combinata con qualsiasi altra costante con un nome che inizia con "LOCALE_I". | 




 

 

 




