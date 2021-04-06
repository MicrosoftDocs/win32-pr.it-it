---
title: Chiave filetype
description: Usato da GetClassFile per trovare la corrispondenza dei modelli con diversi byte di file in un file non composto.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Chiave del registro di sistema filetype COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045280"
---
# <a name="filetype-key"></a><span data-ttu-id="23f13-104">Chiave filetype</span><span class="sxs-lookup"><span data-stu-id="23f13-104">FileType Key</span></span>

<span data-ttu-id="23f13-105">Usato da [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) per trovare la corrispondenza dei modelli con diversi byte di file in un file non composto.</span><span class="sxs-lookup"><span data-stu-id="23f13-105">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="23f13-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="23f13-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span data-ttu-id="23f13-107"><span id="offset"></span><span id="OFFSET"></span>*offset*</span><span class="sxs-lookup"><span data-stu-id="23f13-107"><span id="offset"></span><span id="OFFSET"></span>*offset*</span></span>
</dt> <dd>

<span data-ttu-id="23f13-108">Determina la distanza dall'inizio o dalla fine del file per iniziare il confronto.</span><span class="sxs-lookup"><span data-stu-id="23f13-108">Determines how far from the beginning or end of the file to begin the comparison.</span></span> <span data-ttu-id="23f13-109">Se l'offset è un valore negativo, il confronto inizia dalla fine del file meno il valore di offset.</span><span class="sxs-lookup"><span data-stu-id="23f13-109">If the offset is a negative value, the comparison begins from the end of the file minus the offset value.</span></span> <span data-ttu-id="23f13-110">Il valore di offset è un tipo decimale, a meno che non sia preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="23f13-110">The offset value is a decimal type unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="23f13-111"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="23f13-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="23f13-112">Rappresenta la lunghezza in byte dall'inizio alla fine del file.</span><span class="sxs-lookup"><span data-stu-id="23f13-112">Represents the length in bytes from the beginning to the end of the file.</span></span> <span data-ttu-id="23f13-113">Rappresenta l'intervallo di byte nel file.</span><span class="sxs-lookup"><span data-stu-id="23f13-113">Represents the byte range in the file.</span></span> <span data-ttu-id="23f13-114">Il valore *CB* è un numero decimale, a meno che non sia preceduto da "0x".</span><span class="sxs-lookup"><span data-stu-id="23f13-114">The *cb* value is a decimal unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="23f13-115"><span id="mask"></span><span id="MASK"></span>*maschera*</span><span class="sxs-lookup"><span data-stu-id="23f13-115"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="23f13-116">Valore binario utilizzato per la maschera, che viene eseguito utilizzando un'operazione AND logica e l'intervallo di byte specificato da *offset* e *CB*.</span><span class="sxs-lookup"><span data-stu-id="23f13-116">A binary value used for masking, which is performed by using a logical AND operation, and the byte range specified by *offset* and *cb*.</span></span> <span data-ttu-id="23f13-117">Se questo valore viene omesso, i byte vengono impostati su tutti quelli.</span><span class="sxs-lookup"><span data-stu-id="23f13-117">If this value is omitted, the bytes are set to all ones.</span></span> <span data-ttu-id="23f13-118">Questo valore è sempre esadecimale.</span><span class="sxs-lookup"><span data-stu-id="23f13-118">This value is always hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="23f13-119"><span id="value"></span><span id="VALUE"></span>*valore*</span><span class="sxs-lookup"><span data-stu-id="23f13-119"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="23f13-120">Rappresenta il criterio che deve corrispondere a un file di questo tipo di file.</span><span class="sxs-lookup"><span data-stu-id="23f13-120">Represents the pattern that must match for a file to be of this file type.</span></span> <span data-ttu-id="23f13-121">Il modello viene usato per identificare correttamente un formato di file noto dal contenuto, non dalla relativa estensione.</span><span class="sxs-lookup"><span data-stu-id="23f13-121">The pattern is used to properly identify a known file format from its contents, not by its extension.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23f13-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="23f13-122">Remarks</span></span>

<span data-ttu-id="23f13-123">Le voci vengono usate dalla funzione [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) per trovare la corrispondenza dei modelli con i diversi byte di file in un file non composto.</span><span class="sxs-lookup"><span data-stu-id="23f13-123">Entries are used by the [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) function to match patterns against various file bytes in a non-compound file.</span></span> <span data-ttu-id="23f13-124">**FileType** dispone di sottochiavi CLSID, ognuna delle quali contiene una serie di sottochiavi **0**, **1**, **2**, **3**.</span><span class="sxs-lookup"><span data-stu-id="23f13-124">**FileType** has CLSID subkeys, each of which has a series of subkeys **0**, **1**, **2**, **3**.</span></span> <span data-ttu-id="23f13-125">Questi valori contengono modelli che, se uno corrisponde, producono il CLSID indicato.</span><span class="sxs-lookup"><span data-stu-id="23f13-125">These values contain patterns that, if one matches, yield the indicated CLSID.</span></span> <span data-ttu-id="23f13-126">Ad esempio, il valore "0, 4, FFFFFFFF, ABCD1234" indica che i primi 4 byte devono essere ABCD1234, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="23f13-126">For example, a value of "0, 4, FFFFFFFF, ABCD1234" indicates that the first 4 bytes must be ABCD1234, in that order.</span></span> <span data-ttu-id="23f13-127">Il valore "-4, 4, FEFEFEFE" indica che gli ultimi quattro byte nel file devono essere FEFEFEFE.</span><span class="sxs-lookup"><span data-stu-id="23f13-127">A value of "-4, 4, FEFEFEFE " indicates that the last four bytes in the file must be FEFEFEFE.</span></span> <span data-ttu-id="23f13-128">Se uno dei due criteri corrisponde, viene restituito il CLSID.</span><span class="sxs-lookup"><span data-stu-id="23f13-128">If either pattern matches, the CLSID is returned.</span></span>

<span data-ttu-id="23f13-129">La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.</span><span class="sxs-lookup"><span data-stu-id="23f13-129">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23f13-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23f13-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23f13-131">**<estensione di file \_>**</span><span class="sxs-lookup"><span data-stu-id="23f13-131">**<file\_extension>**</span></span>](-file-extension--key.md)
</dt> <dt>

[<span data-ttu-id="23f13-132">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="23f13-132">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




