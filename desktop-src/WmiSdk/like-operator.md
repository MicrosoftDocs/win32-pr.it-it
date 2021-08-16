---
description: L'operatore LIKE determina se una stringa di caratteri corrisponde o meno a un criterio specificato.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Operatore LIKE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e5df500091fac8b15bcdcb448b7a97fc00dc62807ba854757e447f07e6f4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317870"
---
# <a name="like-operator"></a>Operatore LIKE

L'operatore LIKE determina se una stringa di caratteri corrisponde o meno a un criterio specificato. Il modello specificato può contenere esattamente i caratteri di cui trovare una corrispondenza oppure può contenere meta caratteri. In effetti, l'operatore LIKE corrisponde alle sottostringhe usando i caratteri jolly nella tabella seguente.



| Carattere       | Descrizione                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | Qualsiasi carattere compreso nell'intervallo specificato ( \[ a-f \] ) o impostato ( \[ abcdef \] ).                                                                                                                 |
| ^               | Qualsiasi carattere non compreso nell'intervallo ( \[ ^a-f \] ) o impostato ( \[ ^abcdef \] ).                                                                                                                     |
| %               | Qualsiasi stringa di 0 (zero) o più caratteri. L'esempio seguente trova tutte le istanze in cui "Win" si trova in qualsiasi punto del nome della classe: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ (carattere di sottolineatura) | Qualsiasi carattere. Qualsiasi carattere di sottolineatura letterale usato nella stringa di query deve essere preceduto da un carattere di escape \[ \] inserendolo all'interno (parentesi quadre).                                                             |



 

Ad esempio, il codice power shell seguente recupera tutte le istanze della **classe \_ operatingSystem Win32** la cui **proprietà Name** inizia con **FirstName**:

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Poiché il carattere di sottolineatura è un carattere meta, se la destinazione della query ha un carattere di sottolineatura, i \[ \] caratteri di escape " " devono racchiuderlo. Ad esempio, è possibile eseguire una query per tutte le classi che hanno un doppio carattere di sottolineatura nel nome.

Per individuare tutte le classi con un doppio carattere di sottolineatura nel nome, è necessario eseguire l'escape di entrambi i caratteri di sottolineatura \[ \] con (parentesi quadre), ad esempio:

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

È possibile negare un'istruzione LIKE usando NOT. A tale scopo, assicurarsi di posizionare NOT direttamente davanti al nome del campo. Esempio:

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operatori WQL](wql-operators.md)
</dt> </dl>

 

 



