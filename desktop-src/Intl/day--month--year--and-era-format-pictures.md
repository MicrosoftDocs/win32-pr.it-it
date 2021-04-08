---
description: L'applicazione utilizza gli elementi descritti in questo argomento per costruire una stringa dell'immagine di formato con terminazione null.
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: Immagini del formato giorno, mese, anno ed era
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83439cc33c1caf067b5c6f41234a6f1ddc4dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884578"
---
# <a name="day-month-year-and-era-format-pictures"></a>Immagini del formato giorno, mese, anno ed era

L'applicazione utilizza gli elementi descritti in questo argomento per costruire una stringa dell'immagine di formato con terminazione null. Se vengono usati spazi per separare gli elementi nella stringa, questi spazi verranno visualizzati nella stessa posizione della stringa di output.

> [!Note]  
> I tipi di formato "d", "g" e "y" devono essere minuscoli e la lettera "M" deve essere in maiuscolo.

 

Ad esempio, per ottenere la stringa di data "Mer, Aug 31 94", l'applicazione usa la stringa immagine "ddd", "MMM DD AA".

L'applicazione usa le virgolette singole per contrassegnare i caratteri da visualizzare esattamente come specificato. Se l'applicazione deve visualizzare una virgoletta singola, deve inserire due virgolette singole in una riga. Ad esempio,' ABC '' barra ' viene visualizzato come "abc'bar".

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare i giorni.



| Tipo di formato | Significato                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d           | Giorno del mese come cifre senza zeri iniziali per i giorni a una sola cifra.                                                                                                                                                                                                                                                                                                   |
| gg          | Giorno del mese come cifre con zeri iniziali per i giorni a una sola cifra.                                                                                                                                                                                                                                                                                                      |
| ddd         | Il giorno della settimana abbreviato come specificato da un valore di [ \_ SABBREVDAYNAME \* delle impostazioni locali](locale-sabbrev-constants.md) , ad esempio, "lun" in inglese (Stati Uniti).**Windows Vista e versioni successive:** se è richiesta una versione breve del giorno della settimana, l'applicazione deve usare le costanti [ \_ SSHORTESTDAYNAME \* delle impostazioni locali](locale-sshortestdayname-constants.md) .<br/> |
| dddd        | Giorno della settimana come specificato da un valore [ \_ SDAYNAME \* delle impostazioni locali](locale-sdayname-constants.md) .                                                                                                                                                                                                                                                                              |



 

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare i mesi.



| Tipo di formato | Significato                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M           | Mese come cifre senza zeri iniziali per i mesi a una sola cifra.                                                                                                                   |
| MM          | Mese come cifre con zeri iniziali per i mesi a una sola cifra.                                                                                                                      |
| MMM         | Il mese abbreviato come specificato da un valore [ \_ SABBREVMONTHNAME \* delle impostazioni locali](locale-sabbrev-constants.md) , ad esempio, "nov" in inglese (Stati Uniti).                             |
| MMMM        | Mese come specificato da un valore [ \_ SMONTHNAME \* delle impostazioni locali](locale-smonthname-constants.md) , ad esempio "novembre" per l'inglese (Stati Uniti) e "Noviembre" per lo spagnolo (Spagna). |



 

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare gli anni.



| Tipo di formato | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| y           | Anno rappresentato solo dall'ultima cifra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| yy          | Anno rappresentato solo dalle ultime due cifre. Viene aggiunto uno zero iniziali per gli anni a una sola cifra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| aaaa        | Anno rappresentato da un massimo di quattro o cinque cifre, a seconda del calendario usato. I calendari tailandesi thailandesi e coreano hanno anni a cinque cifre. Il modello "aaaa" Mostra cinque cifre per questi due calendari e quattro cifre per tutti gli altri calendari supportati. I calendari con anni a singola cifra o a due cifre, ad esempio per l'era giapponese dell'imperatore, sono rappresentati in modo diverso. Un anno a una sola cifra viene rappresentato con uno zero principale, ad esempio "03". Un anno a due cifre è rappresentato da due cifre, ad esempio, "13". Non vengono visualizzati altri zeri iniziali. |
| yyyyy       | Si comporta in modo identico a "aaaa".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

La tabella seguente definisce i tipi di formato usati per rappresentare un punto o un'era.



| Tipo di formato | Significato                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g, GG       | Stringa period/era formattata come specificata dal \_ valore Cal SERASTRING. Le immagini di formato "g" e "gg" in una stringa di data vengono ignorate se non è presente alcuna stringa di periodo o di era associata. |



 

 

 




