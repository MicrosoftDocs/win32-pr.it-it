---
description: L'applicazione usa gli elementi descritti in questo argomento per costruire una stringa di immagine in formato con terminazione Null.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Immagini in formato giorno, mese, anno ed era
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ae1adf82a202ebb08f199bb252e59c0f35aab8ad35b60ac57a8ebbe102711c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068271"
---
# <a name="day-month-year-and-era-format-pictures"></a>Immagini in formato giorno, mese, anno ed era

L'applicazione usa gli elementi descritti in questo argomento per costruire una stringa di immagine in formato con terminazione Null. Se vengono usati spazi per separare gli elementi nella stringa, questi spazi verranno visualizzati nella stessa posizione nella stringa di output.

> [!Note]  
> I tipi di formato "d", "g" e "y" devono essere minuscoli e la lettera "M" deve essere maiuscola.

 

Ad esempio, per ottenere la stringa di data "Wed, Aug 31 94", l'applicazione usa la stringa di immagine "ddd',' MMM dd yy".

L'applicazione usa virgolette singole per contrassegnare i caratteri da visualizzare esattamente come specificato. Se l'applicazione deve visualizzare una virgoletta singola, deve inserire due virgolette singole in una riga. Ad esempio, 'abc''bar' viene visualizzato come "abc'bar".

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare i giorni.



| Tipo di formato | Significato                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Giorno del mese come cifre senza zeri iniziali per i giorni a una cifra.                                                                                                                                                                                                                                                                                                   |
| gg          | Giorno del mese sotto forma di cifre con zeri iniziali per i giorni a una cifra.                                                                                                                                                                                                                                                                                                      |
| ddd         | Giorno abbreviato della settimana come specificato da un valore [ \_ LOCALE SABBREVDAYNAME, \*](locale-sabbrev-constants.md) ad esempio "Mon" in inglese (Stati Uniti).**Windows Vista e versioni successive:** se è necessaria una versione abbreviata del giorno della settimana, l'applicazione deve usare le costanti [LOCALE \_ SSHORTESTDAYNAME. \*](locale-sshortestdayname-constants.md)<br/> |
| dddd        | Giorno della settimana come specificato da un [valore \_ LOCALE SDAYNAME. \* ](locale-sdayname-constants.md)                                                                                                                                                                                                                                                                              |



 

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare i mesi.



| Tipo di formato | Significato                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Mese come cifre senza zeri iniziali per i mesi a una cifra.                                                                                                                   |
| MM          | Mese come cifre con zeri iniziali per i mesi a una cifra.                                                                                                                      |
| MMM         | Mese abbreviato come specificato da un valore [ \_ LOCALE SABBREVMONTHNAME, \* ](locale-sabbrev-constants.md) ad esempio "Nov" in inglese (Stati Uniti).                             |
| MMMM        | Mese come specificato da un valore [ \_ LOCALE SMONTHNAME, \* ](locale-smonthname-constants.md) ad esempio "Novembre" per l'inglese (Stati Uniti) e "Noviembre" per spagnolo (Spagna). |



 

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare gli anni.



| Tipo di formato | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| y           | Anno rappresentato solo dall'ultima cifra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Anno rappresentato solo dalle ultime due cifre. Per gli anni a una cifra viene aggiunto uno zero iniziale.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| aaaa        | Anno rappresentato da quattro o cinque cifre complete, a seconda del calendario usato. I calendari thai e coreano hanno anni a cinque cifre. Il modello "yyyy" mostra cinque cifre per questi due calendari e quattro cifre per tutti gli altri calendari supportati. I calendari con anni a una o a due cifre, ad esempio per l'era del Giappone, sono rappresentati in modo diverso. Un anno a una cifra è rappresentato da uno zero iniziale, ad esempio "03". Un anno a due cifre è rappresentato da due cifre, ad esempio "13". Non vengono visualizzati zeri iniziali aggiuntivi. |
| yyyyy       | Si comporta in modo identico a "yyyy".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare un periodo o un'era.



| Tipo di formato | Significato                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, gg       | Stringa punto/era formattata come specificato dal valore \_ CAL SERASTRING. Le immagini in formato "g" e "gg" in una stringa di data vengono ignorate se non è presente alcuna stringa di era o punto associata. |



 

 

 




