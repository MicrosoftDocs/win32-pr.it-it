---
description: Fornisce restrizioni per l'utilizzo di valori a 64 bit come parte di un percorso.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Supporto dell'istanza di classe per i valori a 64 bit
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315242"
---
# <a name="class-instance-support-for-64-bit-values"></a><span data-ttu-id="eeaea-103">Supporto dell'istanza di classe per i valori a 64 bit</span><span class="sxs-lookup"><span data-stu-id="eeaea-103">Class Instance Support for 64-Bit Values</span></span>

<span data-ttu-id="eeaea-104">È possibile usare un valore di chiave a 64 bit come parte di un percorso, con le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="eeaea-104">You can use a 64-bit key value as part of a path, with the following restrictions:</span></span>

-   <span data-ttu-id="eeaea-105">Fino a quando non si supera l'intervallo di 32 bit, è possibile assegnare e recuperare i valori dalla chiave come si farebbe con una proprietà a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="eeaea-105">As long as you do not exceed the 32-bit range, you can assign and retrieve values from the key as you would a 32-bit property.</span></span>
-   <span data-ttu-id="eeaea-106">Dopo aver superato il valore integer di 0x7FFFFFFF (per i tipi con segno), 0x80000000 (per i tipi senza segno) o 32 bit, è necessario utilizzare le virgolette.</span><span class="sxs-lookup"><span data-stu-id="eeaea-106">After you exceed the integer value of 0x7FFFFFFF (for signed types), 0x80000000 (for unsigned types), or 32 bits, you must use quotation marks.</span></span>
-   <span data-ttu-id="eeaea-107">L'unico percorso valido per un valore a 64 bit si trova nelle proprietà **\_ \_ RelPath** o **\_ \_ path** dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="eeaea-107">The only valid path for a 64-bit value is located in the **\_\_RELPATH** or **\_\_PATH** properties of the instance.</span></span> <span data-ttu-id="eeaea-108">Di conseguenza, WMI non supporta la notazione esadecimale per il valore equivalente.</span><span class="sxs-lookup"><span data-stu-id="eeaea-108">As such, WMI does not support the hexadecimal notation for the equivalent value.</span></span>
-   <span data-ttu-id="eeaea-109">Se WMI registra la chiave di istanza come numero negativo, è necessario utilizzare il numero originale per recuperare l'istanza.</span><span class="sxs-lookup"><span data-stu-id="eeaea-109">If WMI records the instance key as a negative number, then you must use the original number to retrieve the instance.</span></span>

<span data-ttu-id="eeaea-110">La semantica di query non è interessata e si comporta come previsto.</span><span class="sxs-lookup"><span data-stu-id="eeaea-110">Query semantics are unaffected and behave as expected.</span></span> <span data-ttu-id="eeaea-111">Questo comportamento influiscono solo sulle operazioni Path dell'oggetto, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="eeaea-111">This behavior only affects the object path, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) operations.</span></span>

<span data-ttu-id="eeaea-112">Nell'esempio seguente viene illustrato che le istanze della classe possono avere valori di chiave a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="eeaea-112">The following example shows that class instances can have 64-bit key values.</span></span>

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



