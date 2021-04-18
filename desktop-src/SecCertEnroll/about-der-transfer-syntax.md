---
description: L'applicazione di una regola di codifica alle strutture di dati descritte da una sintassi astratta fornisce una sintassi di trasferimento che determina la modalità di organizzazione dei byte in un flusso quando viene inviato tra computer.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Sintassi di trasferimento DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569194"
---
# <a name="der-transfer-syntax"></a><span data-ttu-id="37ae2-103">Sintassi di trasferimento DER</span><span class="sxs-lookup"><span data-stu-id="37ae2-103">DER Transfer Syntax</span></span>

<span data-ttu-id="37ae2-104">L'applicazione di una regola di codifica alle strutture di dati descritte da una sintassi astratta fornisce una sintassi di trasferimento che determina la modalità di organizzazione dei byte in un flusso quando viene inviato tra computer.</span><span class="sxs-lookup"><span data-stu-id="37ae2-104">Applying an encoding rule to the data structures described by an abstract syntax provides a transfer syntax that governs how bytes in a stream are organized when sent between computers.</span></span> <span data-ttu-id="37ae2-105">La sintassi di trasferimento utilizzata da Distinguished Encoding Rules segue sempre il formato di un *tag, una lunghezza e un valore* .</span><span class="sxs-lookup"><span data-stu-id="37ae2-105">The transfer syntax used by Distinguished Encoding Rules always follows a *Tag, Length, Value* format.</span></span> <span data-ttu-id="37ae2-106">Il formato viene in genere definito tripletta TLV in cui ogni campo (T, L o V) contiene uno o più byte.</span><span class="sxs-lookup"><span data-stu-id="37ae2-106">The format is usually referred to as a TLV triplet in which each field (T, L, or V) contains one or more bytes.</span></span>

![tipo der, lunghezza e tripletta del valore (TLV)](images/der-tlv-basic.png)

<span data-ttu-id="37ae2-108">Il campo *tag* specifica il tipo di struttura dei dati da inviare, il campo *lunghezza* specifica il numero di byte di contenuto da trasferire e il campo *valore* contiene il contenuto.</span><span class="sxs-lookup"><span data-stu-id="37ae2-108">The *Tag* field specifies the type of the data structure being sent, the *Length* field specifies the number of bytes of content being transferred, and the *Value* field contains the content.</span></span> <span data-ttu-id="37ae2-109">Si noti che il campo *valore* può essere una tripletta se contiene un tipo di dati costruito, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="37ae2-109">Note that the *Value* field can be a triplet if it contains a constructed data type as shown by the following illustration.</span></span>

![ricorsione tripletta der TLV](images/der-tlv-recursive.png)

<span data-ttu-id="37ae2-111">Per informazioni dettagliate sui componenti di una tripletta TLV, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="37ae2-111">See the following topics for detailed information about the components of a TLV triplet.</span></span>

-   [<span data-ttu-id="37ae2-112">Byte tag codificati</span><span class="sxs-lookup"><span data-stu-id="37ae2-112">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
-   [<span data-ttu-id="37ae2-113">Byte di lunghezza e valore codificati</span><span class="sxs-lookup"><span data-stu-id="37ae2-113">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a><span data-ttu-id="37ae2-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37ae2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37ae2-115">Tipi costruiti</span><span class="sxs-lookup"><span data-stu-id="37ae2-115">Constructed Types</span></span>](about-constructed-types.md)
</dt> <dt>

[<span data-ttu-id="37ae2-116">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="37ae2-116">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 



