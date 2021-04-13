---
title: ISAN
description: L'attributo ISAN contiene il numero audiovisivo standard internazionale (ISAN) che identifica il contenuto.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato ISAN Windows Media
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398672"
---
# <a name="isan"></a><span data-ttu-id="3e21f-104">ISAN</span><span class="sxs-lookup"><span data-stu-id="3e21f-104">ISAN</span></span>

<span data-ttu-id="3e21f-105">L'attributo **ISAN** contiene il numero audiovisivo standard internazionale (ISAN) che identifica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="3e21f-105">The **ISAN** attribute contains the International Standard Audiovisual Number (ISAN) that identifies the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3e21f-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="3e21f-106">Global Constant</span></span>

<span data-ttu-id="3e21f-107">g \_ wszISAN</span><span class="sxs-lookup"><span data-stu-id="3e21f-107">g\_wszISAN</span></span>

## <a name="data-type"></a><span data-ttu-id="3e21f-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3e21f-108">Data Type</span></span>

<span data-ttu-id="3e21f-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3e21f-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3e21f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e21f-110">Remarks</span></span>

<span data-ttu-id="3e21f-111">ISAN è uno standard internazionale per l'identificazione dei lavori audiovisivi.</span><span class="sxs-lookup"><span data-stu-id="3e21f-111">ISAN is an international standard for identifying audiovisual works.</span></span> <span data-ttu-id="3e21f-112">Per informazioni su ISAN, visitare il [sito Web](https://www.isan.org/)standard.</span><span class="sxs-lookup"><span data-stu-id="3e21f-112">For information about ISAN, visit the standard's [Web site](https://www.isan.org/).</span></span>

<span data-ttu-id="3e21f-113">L'oggetto dell'editor di metadati verifica la stringa ISAN quando si imposta questo attributo.</span><span class="sxs-lookup"><span data-stu-id="3e21f-113">The metadata editor object verifies the ISAN string when you set this attribute.</span></span> <span data-ttu-id="3e21f-114">La formattazione della stringa accettabile, come descritto nella sezione 4,1 della specifica ISAN, è costituita da 16 cifre esadecimali, separate facoltativamente da spazi vuoti o trattini in segmenti a 4 cifre.</span><span class="sxs-lookup"><span data-stu-id="3e21f-114">The acceptable string formatting, as described in section 4.1 of the ISAN specification, consists of 16 hexadecimal digits, optionally separated by whitespace or hyphens into 4-digit segments.</span></span> <span data-ttu-id="3e21f-115">Il numero formattato deve essere seguito, anch ' esso separato da uno spazio o un trattino, da un carattere di controllo valido.</span><span class="sxs-lookup"><span data-stu-id="3e21f-115">The formatted number must be followed, also optionally separated by a space or hyphen, by a valid check character.</span></span> <span data-ttu-id="3e21f-116">Il carattere di controllo può essere una cifra decimale o una lettera maiuscola.</span><span class="sxs-lookup"><span data-stu-id="3e21f-116">The check character can be a decimal digit or a capital letter.</span></span> <span data-ttu-id="3e21f-117">Per informazioni su come derivare il numero di controllo, vedere l'allegato A del manuale dell'utente di ISAN.</span><span class="sxs-lookup"><span data-stu-id="3e21f-117">Refer to annex A of the ISAN user guide for information about how to derive the check number.</span></span>

<span data-ttu-id="3e21f-118">La stringa ISAN standard può essere seguita dalle informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="3e21f-118">The standard ISAN string may be followed by version information.</span></span> <span data-ttu-id="3e21f-119">Se presente, le informazioni sulla versione sono costituite da otto cifre esadecimali seguite da un numero di controllo.</span><span class="sxs-lookup"><span data-stu-id="3e21f-119">If present, version information consists of eight hexadecimal digits followed by a check number.</span></span> <span data-ttu-id="3e21f-120">La formattazione di questi caratteri segue le stesse regole della stringa di base.</span><span class="sxs-lookup"><span data-stu-id="3e21f-120">The formatting of these characters follows the same rules as the basic string.</span></span>

## <a name="examples"></a><span data-ttu-id="3e21f-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="3e21f-121">Examples</span></span>

<span data-ttu-id="3e21f-122">Di seguito sono riportate tre stringhe formattate in modo accettabile per un esempio ISAN.</span><span class="sxs-lookup"><span data-stu-id="3e21f-122">The following are three acceptably formatted strings for an example ISAN.</span></span>


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



<span data-ttu-id="3e21f-123">La stringa seguente mostra il formato di un ISAN con le informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="3e21f-123">The following string shows the format of an ISAN with version information.</span></span>


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a><span data-ttu-id="3e21f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e21f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e21f-125">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="3e21f-125">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




