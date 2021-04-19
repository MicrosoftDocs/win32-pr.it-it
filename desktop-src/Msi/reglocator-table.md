---
description: La tabella RegLocator include le informazioni necessarie per cercare un file o una directory usando il registro di sistema o per cercare una particolare voce del registro di sistema. Questa tabella contiene le colonne seguenti.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Tabella RegLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311702"
---
# <a name="reglocator-table"></a>Tabella RegLocator

La tabella RegLocator include le informazioni necessarie per cercare un file o una directory usando il registro di sistema o per cercare una particolare voce del registro di sistema. Questa tabella contiene le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificatore](identifier.md) | S   | N        |
| Radice        | [Integer](integer.md)       | N   | N        |
| Chiave         | [RegPath](regpath.md)       | N   | N        |
| Nome        | [Formattato](formatted.md)   | N   | Y        |
| Tipo        | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

Il valore nel campo firma \_ rappresenta una firma univoca che è una chiave esterna nella colonna uno della tabella della [firma](signature-table.md) . Se la firma è presente nella tabella della firma, la ricerca è relativa a un file. Se la firma non è presente nella tabella della firma e il valore della colonna del tipo è **msidbLocatorTypeRawValue**, la ricerca è relativa al nome della chiave del registro di sistema a cui punta la tabella RegLocator. In caso contrario, la ricerca è relativa a una directory a cui fa riferimento la tabella RegLocator.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Radice
</dt> <dd>

Chiave radice predefinita per il valore del registro di sistema.



| Costante                          | Valore esadecimale | Decimal | Chiave radice             |
|-----------------------------------|-------------|---------|----------------------|
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | HKEY\_CLASSI\_RADICE  |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | HKEY\_CORRENTE\_UTENTE  |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | HKEY\_LOCALE\_MACCHINA |
| **msidbRegistryRootUsers**        | 0x003       | 3       | HKEY\_UTENTI          |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave per il valore del registro di sistema.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome del valore del registro di sistema. Se questo valore è null, viene recuperato il valore della chiave senza nome o il valore predefinito, se disponibile.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Valore che determina se il valore del registro di sistema è un nome file, un percorso di directory o un valore del registro di sistema non elaborato.

Nella tabella seguente sono elencati i valori validi. Impostare uno dei primi tre valori e **msidbLocatorType64bit** , se necessario. Se la voce in questo campo è assente, Type è impostato su 1.



| Costante                      | Valore esadecimale | Decimal | Descrizione                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Il percorso della chiave è una directory.                                                                                                                                           |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Il percorso della chiave è un nome di file.                                                                                                                                           |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Il percorso della chiave è un valore del registro di sistema.                                                                                                                                      |
| **msidbLocatorType64bit**     | 0x010       | 16      | Impostare questo bit in modo che il programma di installazione cerchi la parte del registro di sistema a 64 bit. Non impostare questo bit per fare in modo che il programma di installazione cerchi la parte del registro di sistema a 32 bit. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che se il valore nel campo tipo è **msidbLocatorTypeRawValue**, il programma di installazione imposta il valore della proprietà specificata nel campo della proprietà della tabella [AppSearch](appsearch-table.md) sul valore del registro di sistema. Il programma di installazione aggiunge un prefisso al valore del registro di sistema che identifica il tipo di valore del registro di sistema. Per ulteriori informazioni sui tipi di valori del registro di sistema, vedere [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md).



| Tipo di registro   | Prefisso aggiunto dal programma di installazione                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ SZ         | None, ma se il primo carattere del valore del registro di sistema è \# , il programma di installazione evita il carattere anteponendo un altro \# .            |
| DWORD           | " \# " seguito facoltativamente da' +' o da'-'                                                                                                  |
| REG \_ Espandi \_ SZ | "\#%"                                                                                                                                   |
| REG \_ - \_ SZ  | Null. Il programma di installazione imposta la proprietà su un valore che inizia con un valore null e termina con un valore null.                                          |
| REG \_ binario     | " \# x" nel caso del \_ file binario REG, il programma di installazione converte e salva ogni cifra esadecimale (bocconcino) come carattere ASCII preceduto da " \# x". |



 

In genere, le colonne in questa tabella non sono localizzate. Se un autore decide di cercare i prodotti in più lingue, è necessario che nella tabella sia inclusa una voce separata per ogni lingua.

Si noti che non è possibile usare la tabella RegLocator per verificare solo la presenza della chiave. Tuttavia, è possibile cercare il valore predefinito di una chiave e recuperare il relativo valore se non è vuoto.

Per ulteriori informazioni, vedere [ricerca di applicazioni esistenti, file, voci del registro di sistema o voci del file ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE80](ice80.md)  
</dl>

 

 
