---
description: L'operatore LIKE determina se una stringa di caratteri corrisponde a un criterio specificato.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Operatore LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310346"
---
# <a name="like-operator"></a>Operatore LIKE

L'operatore LIKE determina se una stringa di caratteri corrisponde a un criterio specificato. Il modello specificato può contenere esattamente i caratteri per cui trovare una corrispondenza oppure può contenere caratteri meta. In effetti, l'operatore LIKE corrisponde a sottostringhe che usano i caratteri jolly nella tabella seguente.



| Carattere       | Descrizione                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | Qualsiasi carattere compreso nell'intervallo specificato ( \[ a-f \] ) o set ( \[ abcdef \] ).                                                                                                                 |
| ^               | Qualsiasi carattere non compreso nell'intervallo ( \[ ^ a-f \] ) o set ( \[ ^ abcdef \] .)                                                                                                                     |
| %               | Qualsiasi stringa di 0 (zero) o più caratteri. Nell'esempio seguente vengono individuate tutte le istanze in cui "Win" si trova in un punto qualsiasi nel nome della classe: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ sottolineatura | Qualsiasi carattere. Qualsiasi carattere di sottolineatura letterale usato nella stringa di query deve essere preceduto da un carattere di escape inserendolo all'interno di parentesi quadre \[ \] .                                                             |



 

Il codice di Power Shell seguente, ad esempio, recupera tutte le istanze della classe **Win32 \_ OperatingSystem** la cui proprietà **Name** inizia con **FirstName**:

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Poiché il carattere di sottolineatura è un carattere meta, se la destinazione della query ha un carattere di sottolineatura, i \[ \] caratteri di escape "" devono racchiuderlo. Ad esempio, è possibile eseguire una query per tutte le classi con un doppio carattere di sottolineatura nel nome.

Per individuare tutte le classi con un doppio carattere di sottolineatura nel nome, è necessario eseguire l'escape di entrambi i caratteri di sottolineatura con \[ \] (parentesi quadre), ad esempio:

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

È possibile negare un'istruzione LIKE usando NOT; a tale scopo, assicurarsi di collocare l'oggetto non direttamente davanti al nome del campo. Ad esempio:

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operatori WQL](wql-operators.md)
</dt> </dl>

 

 



