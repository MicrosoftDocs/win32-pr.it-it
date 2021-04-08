---
description: 'Altre informazioni su: struttura JET_TUPLELIMITS'
title: Struttura JET_TUPLELIMITS
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968615"
---
# <a name="jet_tuplelimits-structure"></a><span data-ttu-id="589cb-103">Struttura JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="589cb-103">JET_TUPLELIMITS Structure</span></span>


<span data-ttu-id="589cb-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="589cb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tuplelimits-structure"></a><span data-ttu-id="589cb-105">Struttura JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="589cb-105">JET_TUPLELIMITS Structure</span></span>

<span data-ttu-id="589cb-106">La struttura **JET_TUPLELIMITS** consente la personalizzazione delle caratteristiche degli indici di tupla in base all'indice, anziché per ogni singola istanza, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="589cb-106">The **JET_TUPLELIMITS** structure allows customization of the tuple index characteristics on a per-index basis, rather than a per-instance basis, using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="589cb-107">**Windows Server 2003:** La struttura **JET_TUPLELIMITS** è stata introdotta in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="589cb-107">**Windows Server 2003:** The **JET_TUPLELIMITS** structure is introduced in Windows Server 2003.</span></span>

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a><span data-ttu-id="589cb-108">Membri</span><span class="sxs-lookup"><span data-stu-id="589cb-108">Members</span></span>

<span data-ttu-id="589cb-109">**chLengthMin**</span><span class="sxs-lookup"><span data-stu-id="589cb-109">**chLengthMin**</span></span>

<span data-ttu-id="589cb-110">Lunghezza minima di una tupla.</span><span class="sxs-lookup"><span data-stu-id="589cb-110">The minimum length of a tuple.</span></span> <span data-ttu-id="589cb-111">Il valore predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="589cb-111">The default value is 3.</span></span>

<span data-ttu-id="589cb-112">**chLengthMax**</span><span class="sxs-lookup"><span data-stu-id="589cb-112">**chLengthMax**</span></span>

<span data-ttu-id="589cb-113">Lunghezza massima di una tupla.</span><span class="sxs-lookup"><span data-stu-id="589cb-113">The maximum length of a tuple.</span></span> <span data-ttu-id="589cb-114">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="589cb-114">The default value is 10.</span></span>

<span data-ttu-id="589cb-115">**chToIndexMax**</span><span class="sxs-lookup"><span data-stu-id="589cb-115">**chToIndexMax**</span></span>

<span data-ttu-id="589cb-116">Lunghezza massima di una stringa da indicizzare.</span><span class="sxs-lookup"><span data-stu-id="589cb-116">The maximum length of a string to index.</span></span> <span data-ttu-id="589cb-117">Se ad esempio una colonna ha una lunghezza di 100 caratteri e **chToIndexMax** è impostato su 60, verranno indicizzati solo i primi 60 caratteri della colonna.</span><span class="sxs-lookup"><span data-stu-id="589cb-117">For example, if a column is 100 characters long, and **chToIndexMax** is set to 60, then only the first 60 characters of the column will be indexed.</span></span> <span data-ttu-id="589cb-118">Il valore predefinito è 32767.</span><span class="sxs-lookup"><span data-stu-id="589cb-118">The default value is 32767.</span></span>

<span data-ttu-id="589cb-119">**cchIncrement**</span><span class="sxs-lookup"><span data-stu-id="589cb-119">**cchIncrement**</span></span>

<span data-ttu-id="589cb-120">Questo consente di configurare lo stride in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="589cb-120">This allows the stride to be configured on a per index basis.</span></span>

<span data-ttu-id="589cb-121">**Windows Vista:** Il membro **cchIncrement** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="589cb-121">**Windows Vista:** The **cchIncrement** member is introduced in Windows Vista.</span></span> <span data-ttu-id="589cb-122">Prima di Windows Vista, la quantità di spostamento della finestra ("stride") era sempre 1, come illustrato nell'esempio nella sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="589cb-122">Prior to Windows Vista, the amount to shift the window (the "stride") was always 1, as is shown in the example in the remarks section.</span></span>

<span data-ttu-id="589cb-123">**ichStart**</span><span class="sxs-lookup"><span data-stu-id="589cb-123">**ichStart**</span></span>

<span data-ttu-id="589cb-124">Offset nel valore per iniziare a recuperare le tuple dal valore.</span><span class="sxs-lookup"><span data-stu-id="589cb-124">The offset into the value to begin taking retrieving tuples from the value.</span></span>

<span data-ttu-id="589cb-125">**Windows Vista:** Il membro **ichStart** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="589cb-125">**Windows Vista:** The **ichStart** member is introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="589cb-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="589cb-126">Remarks</span></span>

<span data-ttu-id="589cb-127">Un indice tupla percorre una stringa e indicizza tutte le sottostringhe possibili di **chLengthMax**.</span><span class="sxs-lookup"><span data-stu-id="589cb-127">A tuple index walks a string and indexes all of its possible substrings of **chLengthMax**.</span></span> <span data-ttu-id="589cb-128">Alla fine della stringa (o nella posizione **chToIndexMax**, a seconda di quale si verifichi per primo), le sottostringhe di almeno **chLengthMin** verranno indicizzate.</span><span class="sxs-lookup"><span data-stu-id="589cb-128">At the end of the string (or at position **chToIndexMax**, whichever occurs first), the substrings of at least **chLengthMin** will be indexed.</span></span>

<span data-ttu-id="589cb-129">Un indice tupla può essere utilizzato per la ricerca di stringhe con caratteri jolly iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="589cb-129">A tuple index can be used for searching strings with both leading and trailing wildcards.</span></span>

<span data-ttu-id="589cb-130">Supponendo una riga con un campo di testo "RAIN IN SPAIN \! ", se viene creato un indice di tupla con i parametri **chLengthMin**= 2 e **chLengthMax**= 3, nell'indice vengono create le voci seguenti:</span><span class="sxs-lookup"><span data-stu-id="589cb-130">Assuming a row with a text field of "RAIN IN SPAIN\!", if a tuple index gets created with parameters **chLengthMin**=2, and **chLengthMax**=3, the following entries are created in the index:</span></span>

<span data-ttu-id="589cb-131">Rai</span><span class="sxs-lookup"><span data-stu-id="589cb-131">"RAI"</span></span>  
<span data-ttu-id="589cb-132">Ain</span><span class="sxs-lookup"><span data-stu-id="589cb-132">"AIN"</span></span>  
<span data-ttu-id="589cb-133">IN</span><span class="sxs-lookup"><span data-stu-id="589cb-133">"IN "</span></span>  
<span data-ttu-id="589cb-134">"N I"</span><span class="sxs-lookup"><span data-stu-id="589cb-134">"N I"</span></span>  
<span data-ttu-id="589cb-135">IN</span><span class="sxs-lookup"><span data-stu-id="589cb-135">" IN"</span></span>  
<span data-ttu-id="589cb-136">IN</span><span class="sxs-lookup"><span data-stu-id="589cb-136">"IN "</span></span>  
<span data-ttu-id="589cb-137">"N S"</span><span class="sxs-lookup"><span data-stu-id="589cb-137">"N S"</span></span>  
<span data-ttu-id="589cb-138">SP</span><span class="sxs-lookup"><span data-stu-id="589cb-138">" SP"</span></span>  
<span data-ttu-id="589cb-139">Spa</span><span class="sxs-lookup"><span data-stu-id="589cb-139">"SPA"</span></span>  
<span data-ttu-id="589cb-140">Pai</span><span class="sxs-lookup"><span data-stu-id="589cb-140">"PAI"</span></span>  
<span data-ttu-id="589cb-141">Ain</span><span class="sxs-lookup"><span data-stu-id="589cb-141">"AIN"</span></span>  
<span data-ttu-id="589cb-142">"IN \! "</span><span class="sxs-lookup"><span data-stu-id="589cb-142">"IN\!"</span></span>  
<span data-ttu-id="589cb-143">"N \! "</span><span class="sxs-lookup"><span data-stu-id="589cb-143">"N\!"</span></span>

<span data-ttu-id="589cb-144">Si noti che "IN" si verifica due volte e che l'ultima voce ("N \! ") è più corta di 3 (**chLengthMax**).</span><span class="sxs-lookup"><span data-stu-id="589cb-144">Note that "IN " occurs twice, and that the last entry ("N\!") is shorter than 3 (**chLengthMax**).</span></span> <span data-ttu-id="589cb-145">Si noti inoltre che l'algoritmo di suddivisione non è in grado di riconoscere spazi o parole e considera tutti i caratteri in modo identico.</span><span class="sxs-lookup"><span data-stu-id="589cb-145">Also note that the splitting algorithm is not aware of spaces or words, and treats all characters identically.</span></span>

<span data-ttu-id="589cb-146">**Windows XP:** Windows XP supporta gli indici di tupla, ma non **JET_TUPLELIMITS**.</span><span class="sxs-lookup"><span data-stu-id="589cb-146">**Windows XP:** Windows XP supports tuple indexes, but does not have **JET_TUPLELIMITS**.</span></span> <span data-ttu-id="589cb-147">Il motore di database utilizzerà i valori predefiniti (**chLengthMin**= 3, **chLengthMax**= 10, **chToIndexMax**= 32767).</span><span class="sxs-lookup"><span data-stu-id="589cb-147">The database engine will used the default values (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767).</span></span> <span data-ttu-id="589cb-148">È comunque possibile modificare questi valori, ma vengono impostati per ogni singola istanza usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)e [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="589cb-148">It is still possible to change these values, but they are set on a per-instance basis using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md), and [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="589cb-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="589cb-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="589cb-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="589cb-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="589cb-151">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="589cb-151">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="589cb-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="589cb-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="589cb-153">Richiede Windows Server 2008, Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="589cb-153">Requires Windows Server 2008, Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="589cb-154"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="589cb-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="589cb-155">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="589cb-155">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="589cb-156">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="589cb-156">See Also</span></span>

[<span data-ttu-id="589cb-157">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="589cb-157">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="589cb-158">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="589cb-158">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="589cb-159">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="589cb-159">JET_TUPLELIMITS</span></span>]()  
[<span data-ttu-id="589cb-160">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="589cb-160">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
