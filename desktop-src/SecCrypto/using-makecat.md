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
# <a name="using-makecat"></a><span data-ttu-id="914dc-104">Uso di MakeCat</span><span class="sxs-lookup"><span data-stu-id="914dc-104">Using MakeCat</span></span>

<span data-ttu-id="914dc-105">Lo strumento [MakeCat](makecat.md) crea un file di catalogo non firmato, che contiene gli [*hash*](../secgloss/h-gly.md) di un set di file, insieme agli attributi associati di ogni file nel set.</span><span class="sxs-lookup"><span data-stu-id="914dc-105">The [MakeCat](makecat.md) tool makes an unsigned catalog file, which contains the [*hashes*](../secgloss/h-gly.md) of a set of files along with associated attributes of each file in the set.</span></span> <span data-ttu-id="914dc-106">Un file di catalogo consente all'utente di firmare un file (catalogo) invece di firmare molti singoli file.</span><span class="sxs-lookup"><span data-stu-id="914dc-106">A catalog file allows the user to sign one file (the catalog) instead of signing numerous individual files.</span></span>

<span data-ttu-id="914dc-107">Dopo che il file di catalogo non firmato è stato firmato e trasmesso, il ricevitore può confrontare gli hash dei file originali con quelli contenuti nel file di catalogo e verificare che i file siano privi di manomissioni.</span><span class="sxs-lookup"><span data-stu-id="914dc-107">After the unsigned catalog file is signed and transmitted, the receiver can compare the hashes of the original files to the hashes contained within the catalog file and verify that the files are free of tampering.</span></span>

<span data-ttu-id="914dc-108">Prima di utilizzare lo strumento [MakeCat](makecat.md) , l'utente deve preparare un file di definizione del catalogo (con estensione CDF) utilizzando qualsiasi editor di testo.</span><span class="sxs-lookup"><span data-stu-id="914dc-108">Prior to using the [MakeCat](makecat.md) tool, the user must prepare a Catalog Definition File (.cdf), by using any text editor.</span></span> <span data-ttu-id="914dc-109">Il file con estensione CDF contiene l'elenco di file e gli attributi dei file da catalogare (le specifiche sono elencate di seguito).</span><span class="sxs-lookup"><span data-stu-id="914dc-109">The .cdf file contains the list of files and the attributes of the files to be cataloged (the specifications are listed below).</span></span> <span data-ttu-id="914dc-110">Lo strumento MakeCat analizza il file con estensione CDF, verifica l'elenco degli attributi di ogni file elencato, aggiunge gli attributi elencati al catalogo stesso, esegue l'hashing di ognuno dei file elencati e archivia gli hash di ogni file nel file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="914dc-110">The MakeCat tool scans the .cdf file, verifies the list of attributes of each listed file, adds the listed attributes to the catalog itself, hashes each of the listed files, and stores the hashes of each file into the catalog file.</span></span> <span data-ttu-id="914dc-111">Ogni file ha il relativo hash e gli attributi archiviati separatamente nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="914dc-111">Each file has its hash and attributes stored separately within the catalog.</span></span> <span data-ttu-id="914dc-112">Il file di catalogo può quindi essere firmato e trasmesso.</span><span class="sxs-lookup"><span data-stu-id="914dc-112">This catalog file can then be signed and transmitted.</span></span> <span data-ttu-id="914dc-113">Il ricevitore può quindi confrontare l'hash di ogni file all'interno del catalogo con l'hash dei file originali per dimostrare che il contenuto originale è privo di manomissioni.</span><span class="sxs-lookup"><span data-stu-id="914dc-113">The receiver can subsequently compare the hash of each file within the catalog with the hash of the original files to prove that the original content is free of tampering.</span></span> <span data-ttu-id="914dc-114">MakeCat non modifica il file con estensione CDF.</span><span class="sxs-lookup"><span data-stu-id="914dc-114">MakeCat does not modify the .cdf file.</span></span>

<span data-ttu-id="914dc-115">Gli esempi seguenti usano i comandi [MakeCat](makecat.md) .</span><span class="sxs-lookup"><span data-stu-id="914dc-115">The following examples use [MakeCat](makecat.md) commands.</span></span>

-   <span data-ttu-id="914dc-116">Generare un file di catalogo dal file valido. CDF.</span><span class="sxs-lookup"><span data-stu-id="914dc-116">Generate a catalog file from the file Good.cdf.</span></span>

    <span data-ttu-id="914dc-117">**MakeCat-v valido. CDF**</span><span class="sxs-lookup"><span data-stu-id="914dc-117">**MakeCat -v good.cdf**</span></span>

<span data-ttu-id="914dc-118">Un file, valido. CDF, produce un file di catalogo, Good.cat, analizzando i file UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, unsigned. Class e SignedPE.exe.</span><span class="sxs-lookup"><span data-stu-id="914dc-118">A file, Good.cdf, produces a catalog file, Good.cat, by parsing the files UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, Unsigned.Class, and SignedPE.exe.</span></span> <span data-ttu-id="914dc-119">I file analizzati, insieme a Brave. CDF e i Good.cat appena generati, si trovano tutti nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="914dc-119">The parsed files, along with Good.cdf and the newly generated Good.cat, are all in the same directory.</span></span>

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
> <span data-ttu-id="914dc-120">L'ultima voce nel file con estensione CDF deve avere sempre un carattere di nuova riga esplicito alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="914dc-120">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

 

 
