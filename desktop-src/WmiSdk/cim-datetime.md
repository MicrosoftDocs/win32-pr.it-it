---
description: È possibile accedere a tutte le date e ore di Common Information Model (CIM) in WMI utilizzando uno dei due formati a lunghezza fissa specifici di WMI e CIM. Nello scripting usare l'oggetto SWbemDateTime per convertirli in date e ore normali.
ms.assetid: 15126802-82f9-4ab4-98d8-0a15184302e9
ms.tgt_platform: multiple
title: CIM_DATETIME
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee4356050ee340cbf9d1b066f012d32c7185dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316990"
---
# <a name="cim_datetime"></a>\_DateTime CIM

È possibile accedere a tutte le date e ore di [*Common Information Model (CIM)*](gloss-c.md) in WMI utilizzando uno dei due formati a lunghezza fissa specifici di WMI e CIM. Nello scripting usare l'oggetto [**SWbemDateTime**](swbemdatetime.md) per convertirli in date e ore normali.

Nelle sezioni seguenti viene descritto come utilizzare i formati di data e ora WMI.

## <a name="format"></a>Formato

Nella tabella seguente sono elencati i due formati di data e ora utilizzati da WMI.



| Formato                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DATETIME](datetime.md)<br/> *Ad aaaammgghhmmss. mmmmmmsUUU*<br/>                             | Formato in cui vengono archiviati i valori [**DateTime**](datetime.md) CIM. Questo formato è indipendente dalle impostazioni locali, quindi è possibile scrivere uno script che viene eseguito in qualsiasi computer. È necessario utilizzare questo formato per definire una data e un'ora in [*Managed Object Format (MOF)*](gloss-m.md)o quando si scrive in un'istanza di utilizzando l' [API com per WMI](com-api-for-wmi.md) o l' [API di scripting per WMI](scripting-api-for-wmi.md). Per ulteriori informazioni, vedere [modifica di una proprietà dell'istanza](modifying-an-instance-property.md). |
| Formato valido solo nelle query di WMI Query Language (WQL).<br/> *aaaa-mm-GG HH: MM: SS: mmm*<br/> | Questo formato può essere usato negli script che usano i metodi [**SWbemDateTime**](swbemdatetime.md) . Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md) o [esecuzione di query con WQL](querying-with-wql.md). Questo formato non è indipendente dalle impostazioni locali. L'ordine di anno, mese e giorno dipende dall'impostazione del formato locale e della lingua della sessione utente. Ad esempio, mentre il valore predefinito per Stati Uniti inglese è "mm-gg-aaaa hh: mm: SS: mmm", il formato per la maggior parte degli altri paesi o aree geografiche è "aaaa-mm-gg hh: mm: SS: mmm".       |



 

Nella tabella seguente sono elencati i campi dei formati.



| Campo    | Descrizione                                                                                                                                                                                                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *yyyy*   | Anno a quattro cifre (da 0000 a 9999). L'implementazione può limitare l'intervallo supportato. Ad esempio, un'implementazione può supportare solo gli anni da 1980 a 2099.                                                                         |
| *mm*     | Mese a due cifre (da 01 a 12).                                                                                                                                                                                                                |
| *dd*     | Giorno a due cifre del mese (da 01 a 31). Questo valore deve essere appropriato per il mese. Ad esempio, il 31 febbraio non è valido. Tuttavia, l'implementazione non deve verificare la presenza di dati validi.                                            |
| *HH*     | Ora del giorno a due cifre che utilizza il formato a 24 ore (da 00 a 23).                                                                                                                                                                              |
| *MM*     | Minuto a due cifre nell'ora (da 00 a 59).                                                                                                                                                                                                   |
| *SS*     | Numero di secondi di due cifre nel minuto (da 00 a 59).                                                                                                                                                                                      |
| *mmmmmm* | Numero di microsecondi a sei cifre nel secondo (da 000000 a 999999). Non è necessario che l'implementazione supporti la valutazione con questo campo. Tuttavia, questo campo deve essere sempre presente per mantenere la natura a lunghezza fissa della stringa. |
| *mmm*    | Numero di millisecondi di tre cifre nel minuto (da 000 a 999).                                                                                                                                                                             |
| *s*      | Segno più (+) o segno meno (-) per indicare un offset positivo o negativo rispetto all'ora UTC (Coordinated Universal Time).                                                                                                                               |
| *UUU*    | Offset di tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC. Per WMI, è consigliabile, ma non obbligatorio, convertire i tempi in GMT (un offset UTC pari a zero).                                              |



 

È necessario immettere tutti i campi con la lunghezza indicata, usando gli zeri iniziali appropriati per il tipo. Tuttavia, utilizzare asterischi per indicare i campi inutilizzati o come valore jolly. È possibile utilizzare un asterisco ( \* ) ovunque eccetto la clausola **where** di una query. Ad esempio, una data e un'ora con un anno non specificato possono verificarsi in qualsiasi anno. Se si desidera lasciare un campo non specificato, è necessario sostituire l'intero campo con asterischi.

Negli esempi seguenti vengono descritti gli utilizzi validi e non validi degli asterischi:

-   19980416 \* \* \* \* \* \* .000000 + \* \* \* (Legal)
-   1998-04-16 \* \* \* \* \* \* : \* \* \* (non valido)
-   199 \* 0416 \* \* \* \* \* \* .000000 + \* \* \* (non valido)
-   199 \* -04-16 \* \* \* \* \* \* : \* \* \* (non valido)

Se viene utilizzato un valore DateTime per rappresentare un punto nel tempo specifico, tutti i relativi campi devono includere dati. Se viene usato per rappresentare un intervallo di tempo, solo i campi necessari per indicare la durata devono includere i dati.

Nell'esempio seguente viene descritto "April First": una data relativa a un anno non specificato, ma ancora un punto definito se il livello di dettaglio di misurazione è un giorno.

-   \*\*\*\*0401 \* \* \* \* \* \* . 000000 +\*\*\*
-   \*\*\*\*-04-01 \* \* \* \* \* \* : \* \* \* (non valido)

## <a name="setting-utc-offset-and-gmt"></a>Impostazione dell'offset UTC e GMT

Gli esempi seguenti descrivono come è possibile definire un'ora senza un fuso orario inserendo asterischi nel campo UUU dopo il segno più o meno:

-   19980401135809.000000 +\*\*\*
-   19980401135809,000000-\*\*\*
-   1998-04-01 13:58:09: \* \* \* (non valido)

Un'applicazione interpreta un riferimento di data e ora senza zone a un cronometro astratto locale all'interno del sistema operativo in esecuzione. Ad esempio, i computer portatili possono avere orologi interni le cui impostazioni possono o non corrispondere al fuso orario geografico. È possibile interpretare l'ora senza zona sostituendo il fuso orario dell'origine ora astratta corrente anziché il fuso orario locale.

È necessario prestare particolare attenzione al significato dell'offset UTC con date e ore nelle query. In generale, i confronti di equivalenza, maggiore di o minore di funzionano tra due date e ore se la data e l'ora utilizzano la stessa differenza UTC. Quando si gestiscono date e ore che si verificano con diversi offset di fuso orario, è necessario convertire prima le date e le ore in GMT.

Le query che coinvolgono date e ore relative con asterischi in uno o più campi sono significative solo per WMI rispetto all'equivalenza. Inoltre, WMI non consente l'utilizzo di asterischi come caratteri jolly. In WMI, invece, vengono confrontate le date e le ore relative in base ai caratteri.

Negli esempi seguenti vengono descritte due date che una query WMI non considera uguale:

-   19980401135809.000000 +\*\*\*
-   19980401135809.000000 + 000

## <a name="converting-to-filetime-or-vt_date-format"></a>Conversione in formato data FILETIME o VT \_

Il formato [**DateTime**](datetime.md) CIM viene utilizzato solo all'interno di WMI. È possibile eseguire la conversione da e verso il formato WMI e il formato di data FILETIME o VT chiamando \_ i metodi dell'oggetto di scripting [**SWbemDateTime**](swbemdatetime.md) . Una struttura **DateTime** [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) è un valore a 64 bit utilizzato dai sistemi operativi Windows a 32 bit. Il \_ formato data VT è un valore DateTime Variant di automazione utilizzato da Visual Basic e ActiveX. Nella tabella seguente sono elencati i metodi di conversione.



| Metodo                                                         | Descrizione                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime. GetFileTime ha provocato**](swbemdatetime-getfiletime.md) | Ottiene un valore [**DateTime**](datetime.md) nel formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .                |
| [**SWbemDateTime. GetVarDate**](swbemdatetime-getvardate.md)   | Ottiene un valore [**DateTime**](datetime.md) nel \_ formato di data VT.                                         |
| [**SWbemDateTime. SetFileTime**](swbemdatetime-setvardate.md)  | Imposta una proprietà [**DateTime**](datetime.md) utilizzando come input un oggetto [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) date. |
| [**SWbemDateTime. SetVarDate**](swbemdatetime-setvardate.md)   | Imposta una proprietà [**DateTime**](datetime.md) utilizzando \_ come input una data di data VT.                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato di data e ora](date-and-time-format.md)
</dt> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> <dt>

[Attività WMI: date e ore](wmi-tasks--dates-and-times.md)
</dt> <dt>

[Formato intervallo](interval-format.md)
</dt> <dt>

[**SWbemObject. Put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServicesEx. Put**](swbemservicesex-put.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
</dt> <dt>

[**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
</dt> </dl>

 

