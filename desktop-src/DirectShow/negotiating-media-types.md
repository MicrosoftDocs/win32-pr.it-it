---
description: Negoziazione di tipi di supporto
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Negoziazione di tipi di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320805"
---
# <a name="negotiating-media-types"></a><span data-ttu-id="e13a3-103">Negoziazione di tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="e13a3-103">Negotiating Media Types</span></span>

<span data-ttu-id="e13a3-104">Quando il gestore del grafo del filtro chiama il metodo [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , dispone di diverse opzioni per specificare un tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="e13a3-104">When the Filter Graph Manager calls the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, it has several options for specifying a media type:</span></span>

-   <span data-ttu-id="e13a3-105">**Tipo completo:** Se il tipo di supporto è specificato completamente, i pin tentano di connettersi a tale tipo.</span><span class="sxs-lookup"><span data-stu-id="e13a3-105">**Complete type:** If the media type is fully specified, the pins attempt to connect with that type.</span></span> <span data-ttu-id="e13a3-106">In caso affermativo, il tentativo di connessione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e13a3-106">If they cannot, the connection attempt fails.</span></span>
-   <span data-ttu-id="e13a3-107">**Tipo di supporto parziale:** Un tipo di supporto è *parziale* se il tipo principale, il sottotipo o il tipo di formato è \_ null GUID.</span><span class="sxs-lookup"><span data-stu-id="e13a3-107">**Partial media type:** A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span> <span data-ttu-id="e13a3-108">Il valore \_ null GUID funge da "carattere jolly", che indica che qualsiasi valore è accettabile.</span><span class="sxs-lookup"><span data-stu-id="e13a3-108">The value GUID\_NULL acts as a "wildcard," indicating that any value is acceptable.</span></span> <span data-ttu-id="e13a3-109">I pin negoziano un tipo coerente con il tipo parziale.</span><span class="sxs-lookup"><span data-stu-id="e13a3-109">The pins negotiate a type that is consistent with the partial type.</span></span>
-   <span data-ttu-id="e13a3-110">**Nessun tipo di supporto:** Se il gestore del grafo del filtro passa un puntatore **null** , i pin possono accettare qualsiasi tipo di supporto accettabile per entrambi i pin.</span><span class="sxs-lookup"><span data-stu-id="e13a3-110">**No media type:** If the Filter Graph Manager passes a **NULL** pointer, the pins can agree to any media type that is acceptable to both pins.</span></span>

<span data-ttu-id="e13a3-111">Se i pin si connettono, la connessione ha sempre un tipo di supporto completo.</span><span class="sxs-lookup"><span data-stu-id="e13a3-111">If the pins do connect, the connection always has a complete media type.</span></span> <span data-ttu-id="e13a3-112">Lo scopo del tipo di supporto fornito da Filter Graph Manager è limitare i tipi di connessione possibili.</span><span class="sxs-lookup"><span data-stu-id="e13a3-112">The purpose of the media type given by the Filter Graph Manager is to limit the possible connection types.</span></span>

<span data-ttu-id="e13a3-113">Durante il processo di negoziazione, il pin di output propone un tipo di supporto chiamando il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="e13a3-113">During the negotiation process, the output pin proposes a media type by calling the input pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="e13a3-114">Il pin di input può accettare o rifiutare il tipo proposto.</span><span class="sxs-lookup"><span data-stu-id="e13a3-114">The input pin can accept or reject the proposed type.</span></span> <span data-ttu-id="e13a3-115">Questo processo si ripete fino a quando il pin di input non accetta un tipo o il pin di output esaurisce i tipi e la connessione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e13a3-115">This process repeats until either the input pin accepts a type, or the output pin runs out of types and the connection fails.</span></span>

<span data-ttu-id="e13a3-116">Il modo in cui un pin di output seleziona i tipi di supporto da proporre dipende dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="e13a3-116">How an output pin selects media types to propose depends on the implementation.</span></span> <span data-ttu-id="e13a3-117">Nelle classi base di DirectShow, il pin di output chiama [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="e13a3-117">In the DirectShow base classes, the output pin calls [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) on the input pin.</span></span> <span data-ttu-id="e13a3-118">Questo metodo restituisce un enumeratore che enumera i tipi di supporti preferiti del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="e13a3-118">This method returns an enumerator that enumerates the input pin's preferred media types.</span></span> <span data-ttu-id="e13a3-119">In caso contrario, il pin di output enumera i propri tipi preferiti.</span><span class="sxs-lookup"><span data-stu-id="e13a3-119">Failing that, the output pin enumerates its own preferred types.</span></span>

<span data-ttu-id="e13a3-120">**Uso dei tipi di supporto**</span><span class="sxs-lookup"><span data-stu-id="e13a3-120">**Working with Media Types**</span></span>

<span data-ttu-id="e13a3-121">In qualsiasi funzione che riceve un parametro del **\_ \_ tipo di supporto am** , convalidare sempre i valori di **cbFormat** e **formatType** prima di dereferenziare il membro **pbFormat** .</span><span class="sxs-lookup"><span data-stu-id="e13a3-121">In any function that receives an **AM\_MEDIA\_TYPE** parameter, always validate the values of **cbFormat** and **formattype** before dereferencing the **pbFormat** member.</span></span> <span data-ttu-id="e13a3-122">Il codice seguente non è corretto:</span><span class="sxs-lookup"><span data-stu-id="e13a3-122">The following code is incorrect:</span></span>


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



<span data-ttu-id="e13a3-123">Il codice seguente è corretto:</span><span class="sxs-lookup"><span data-stu-id="e13a3-123">The following code is correct:</span></span>


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



