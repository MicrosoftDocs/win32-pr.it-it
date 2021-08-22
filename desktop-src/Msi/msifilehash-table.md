---
description: La tabella MsiFileHash viene usata per archiviare un hash a 128 bit di un file di origine fornito dal pacchetto Windows Installer. L'hash viene suddiviso in quattro valori a 32 bit e archiviato in colonne separate della tabella.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Tabella MsiFileHash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc43c7fd812781057ec0be271ffc370a6b5eb2e3054926e1f969383c0fb390c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944948"
---
# <a name="msifilehash-table"></a>Tabella MsiFileHash

La **tabella MsiFileHash** viene usata per archiviare un hash a 128 bit di un file di origine fornito dal pacchetto Windows Installer. L'hash viene suddiviso in quattro valori a 32 bit e archiviato in colonne separate della tabella.

Windows Il programma di installazione può usare l'hashing dei file come mezzo per rilevare ed eliminare la copia di file non necessaria. Un hash di file archiviato nella tabella **MsiFileHash** può essere confrontato con un hash di un file esistente nel computer dell'utente ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). La **tabella MsiFileHash** può essere usata solo con file senza versione.

La **tabella MsiFileHash** include le colonne seguenti.



| Colonna    | Tipo                               | Chiave | Nullable |
|-----------|------------------------------------|-----|----------|
| file\_    | [Identificatore](identifier.md)       | S   | N        |
| Opzioni   | [Integer](integer.md)             | N   | N        |
| HashPart1 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart2 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart3 | [DoubleInteger](doubleinteger.md) | N   | N        |
| Hashpart4 | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna nella [tabella File](file-table.md). Stringa di 72 caratteri.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opzioni
</dt> <dd>

Questa colonna deve essere 0 ed è riservata per un uso futuro.

</dd> <dt>

<span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1
</dt> <dd>

Primi 32 bit di hash. L'hash del file immesso in questo campo deve essere ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o il [**metodo FileHash**](installer-filehash.md). Non usare altri metodi.

</dd> <dt>

<span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2
</dt> <dd>

Secondi 32 bit di hash. L'hash del file immesso in questo campo deve essere ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o il [**metodo FileHash**](installer-filehash.md). Non usare altri metodi di hash.

</dd> <dt>

<span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3
</dt> <dd>

Terzo 32 bit di hash. L'hash del file immesso in questo campo deve essere ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o il [**metodo FileHash**](installer-filehash.md). Non usare altri metodi.

</dd> <dt>

<span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4
</dt> <dd>

Quarto 32 bit di hash. L'hash del file immesso in questo campo deve essere ottenuto chiamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o il [**metodo FileHash**](installer-filehash.md). Non usare altri metodi.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE60](ice60.md)  
[ICE66](ice66.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[Controllo delle versioni dei file predefinito](default-file-versioning.md)
</dt> </dl>

 

 



