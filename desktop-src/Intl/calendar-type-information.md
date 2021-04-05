---
description: In questo argomento vengono descritte le informazioni sul tipo di calendario (tipo di dati CALTYPE) utilizzate nelle funzioni EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo e GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Informazioni sul tipo di calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884590"
---
# <a name="calendar-type-information"></a>Informazioni sul tipo di calendario

In questo argomento vengono descritte le informazioni sul tipo di calendario (tipo di dati CALTYPE) utilizzate nelle funzioni [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)e [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) . Alcuni di questi valori vengono usati anche dalla funzione [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .

Le costanti CALTYPE seguenti possono essere utilizzate in combinazione con qualsiasi altra costante di CALTYPE.



| Costante                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_NOUSEROVERRIDE Cal          | **Windows Me/98, windows 2000:** Utilizzare l'impostazione predefinita del sistema anziché la scelta dell'utente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ nomi dei genitivi restituiti da Cal \_ | **Windows 7 e versioni successive:** Recuperare il risultato da [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) nel formato dei nomi di genial of months, ovvero i nomi usati quando i nomi dei mesi vengono combinati con altri elementi. Ad esempio, in ucraino l'equivalente di gennaio viene scritto come "Січень" quando il mese è denominato da solo. Tuttavia, quando il nome del mese viene usato in combinazione, ad esempio, in una data, ad esempio il 5 gennaio 2003, viene usata la forma genitiva del nome. Per l'esempio ucraino, il nome del mese del genico viene visualizzato come "5 січня 2003". Per ulteriori informazioni, vedere la pagina relativa alle [impostazioni locali \_ restituiscono \_ \_ nomi di genitivi](locale-return-constants.md). |
| \_numero restituito \_ Cal          | **Windows Me/98, windows 2000:** Recuperare il risultato da [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) come numero anziché come stringa. Questa operazione è valida solo per i valori che iniziano con CAL \_ I.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CAL \_ usare \_ CP \_ ACP            | **Windows Me/98, windows 2000:** Usare la tabella codici ANSI di sistema (ACP) invece della tabella codici delle impostazioni locali per la conversione di stringhe. Questa operazione è rilevante solo per le versioni ANSI delle funzioni, ad esempio **EnumCalendarInfoA**.                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Le costanti CALTYPE seguenti si escludono reciprocamente e non possono essere usate in combinazione tra loro in una chiamata di funzione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAL_ICALINTVALUE</td>
<td>Valore integer che indica il tipo di calendario del calendario alternativo.</td>
</tr>
<tr class="even">
<td>CAL_ITWODIGITYEARMAX</td>
<td><strong>Windows Me/98, windows 2000:</strong> Valore intero che indica il limite superiore dell'intervallo dell'anno a due cifre.</td>
</tr>
<tr class="odd">
<td>CAL_IYEAROFFSETRANGE</td>
<td>Una o più stringhe con terminazione null che specificano gli offset dell'anno per ogni intervallo di era. L'ultima stringa ha un carattere null di terminazione aggiuntivo. Questo valore varia in formato a seconda del tipo di calendario facoltativo.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME1</td>
<td>Nome nativo abbreviato del primo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME2</td>
<td>Nome nativo abbreviato del secondo giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME3</td>
<td>Nome nativo abbreviato del terzo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME4</td>
<td>Nome nativo abbreviato del quarto giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME5</td>
<td>Nome nativo abbreviato del quinto giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME6</td>
<td>Nome nativo abbreviato del sesto giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME7</td>
<td>Nome nativo abbreviato del settimo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVERASTRING</td>
<td><strong>Windows 7 e versioni successive:</strong> Nome nativo abbreviato di un'era. L'intera era rappresentata dalla costante CAL_SERASTRING.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME1</td>
<td>Nome nativo abbreviato del primo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME2</td>
<td>Nome nativo abbreviato del secondo mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME3</td>
<td>Nome nativo abbreviato del terzo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME4</td>
<td>Nome nativo abbreviato del quarto mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME5</td>
<td>Nome nativo abbreviato del quinto mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME6</td>
<td>Nome nativo abbreviato del sesto mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME7</td>
<td>Nome nativo abbreviato del settimo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME8</td>
<td>Nome nativo abbreviato dell'ottavo mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME9</td>
<td>Nome nativo abbreviato del nono mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME10</td>
<td>Nome nativo abbreviato del decimo mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME11</td>
<td>Nome nativo abbreviato dell'undicesimo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME12</td>
<td>Nome nativo abbreviato del dodicesimo mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME13</td>
<td>Nome nativo abbreviato del tredicesimo mese dell'anno, se esistente.</td>
</tr>
<tr class="odd">
<td>CAL_SCALNAME</td>
<td>Nome nativo del calendario alternativo.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME1</td>
<td>Nome nativo del primo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME2</td>
<td>Nome nativo del secondo giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME3</td>
<td>Nome nativo del terzo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME4</td>
<td>Nome nativo del quarto giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME5</td>
<td>Nome nativo del quinto giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME6</td>
<td>Nome nativo del sesto giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME7</td>
<td>Nome nativo del settimo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SERASTRING</td>
<td>Una o più stringhe con terminazione null che specificano ognuno dei punti di codice Unicode che specificano l'era associata a CAL_IYEAROFFSETRANGE. L'ultima stringa ha un carattere null di terminazione aggiuntivo. Questo valore varia in formato a seconda del tipo di calendario facoltativo.</td>
</tr>
<tr class="even">
<td>CAL_SLONGDATE</td>
<td>Formati di data estesa per il tipo di calendario.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHDAY</td>
<td><strong>Windows 7 e versioni successive:</strong> Formato del mese e del giorno per il tipo di calendario. La formattazione è simile a quella per CAL_SLONGDATE. Ad esempio, se il modello mese/giorno è il nome completo del mese seguito dal numero di giorno con zeri iniziali, ad esempio il &quot; 03 settembre &quot; , il formato è &quot; MMMM dd &quot; . È possibile utilizzare le virgolette singole per inserire caratteri non di formato, ad esempio, "de" in spagnolo.
<blockquote>
[!Note]<br />
Questo tipo di calendario supporta un solo formato.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME1</td>
<td>Nome nativo del primo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME2</td>
<td>Nome nativo del secondo mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME3</td>
<td>Nome nativo del terzo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME4</td>
<td>Nome nativo del quarto mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME5</td>
<td>Nome nativo del quinto mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME6</td>
<td>Nome nativo del sesto mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME7</td>
<td>Nome nativo del settimo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME8</td>
<td>Nome nativo dell'ottavo mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME9</td>
<td>Nome nativo del nono mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME10</td>
<td>Nome nativo del decimo mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME11</td>
<td>Nome nativo dell'undicesimo mese dell'anno.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME12</td>
<td>Nome nativo del dodicesimo mese dell'anno.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME13</td>
<td>Nome nativo del tredicesimo mese dell'anno, se esistente.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTDATE</td>
<td>Formati di data breve per il tipo di calendario.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME1</td>
<td><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del primo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME2</td>
<td><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del secondo giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME3</td>
<td><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del terzo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME4</td>
<td><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del quarto giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME5</td>
<td><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del quinto giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME6</td>
<td><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del sesto giorno della settimana.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME7</td>
<td><strong>Windows Vista e versioni successive:</strong> Nome nativo breve del settimo giorno della settimana.</td>
</tr>
<tr class="odd">
<td>CAL_SYEARMONTH</td>
<td><strong>Windows Me/98, windows 2000:</strong> Formati anno/mese per i calendari specificati.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Se il nome nativo per il giorno della settimana o per un mese è una stringa vuota, tale nome è identico al nome specificato nelle informazioni sulle impostazioni locali corrispondenti e pertanto non viene duplicato qui.

 

 

 




