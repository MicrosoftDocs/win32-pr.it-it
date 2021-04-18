---
description: Crea un file di catalogo non firmato, che contiene gli hash di un set di file insieme agli attributi associati di ogni file nel set. Un file di catalogo consente all'utente di firmare un file (catalogo) invece di firmare molti singoli file.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Uso di MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308634"
---
# <a name="using-makecat"></a>Uso di MakeCat

Lo strumento [MakeCat](makecat.md) crea un file di catalogo non firmato, che contiene gli [*hash*](../secgloss/h-gly.md) di un set di file, insieme agli attributi associati di ogni file nel set. Un file di catalogo consente all'utente di firmare un file (catalogo) invece di firmare molti singoli file.

Dopo che il file di catalogo non firmato è stato firmato e trasmesso, il ricevitore può confrontare gli hash dei file originali con quelli contenuti nel file di catalogo e verificare che i file siano privi di manomissioni.

Prima di utilizzare lo strumento [MakeCat](makecat.md) , l'utente deve preparare un file di definizione del catalogo (con estensione CDF) utilizzando qualsiasi editor di testo. Il file con estensione CDF contiene l'elenco di file e gli attributi dei file da catalogare (le specifiche sono elencate di seguito). Lo strumento MakeCat analizza il file con estensione CDF, verifica l'elenco degli attributi di ogni file elencato, aggiunge gli attributi elencati al catalogo stesso, esegue l'hashing di ognuno dei file elencati e archivia gli hash di ogni file nel file di catalogo. Ogni file ha il relativo hash e gli attributi archiviati separatamente nel catalogo. Il file di catalogo può quindi essere firmato e trasmesso. Il ricevitore può quindi confrontare l'hash di ogni file all'interno del catalogo con l'hash dei file originali per dimostrare che il contenuto originale è privo di manomissioni. MakeCat non modifica il file con estensione CDF.

Gli esempi seguenti usano i comandi [MakeCat](makecat.md) .

-   Generare un file di catalogo dal file valido. CDF.

    **MakeCat-v valido. CDF**

Un file, valido. CDF, produce un file di catalogo, Good.cat, analizzando i file UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, unsigned. Class e SignedPE.exe. I file analizzati, insieme a Brave. CDF e i Good.cat appena generati, si trovano tutti nella stessa directory.

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> L'ultima voce nel file con estensione CDF deve avere sempre un carattere di nuova riga esplicito alla fine della riga.

 

 

 
