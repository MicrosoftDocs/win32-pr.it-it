---
description: Il nome di colonna riservato \_ RowState rappresenta lo stato non persistente associato a ogni riga della tabella in una tabella di database del programma di installazione.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState colonna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049918"
---
# <a name="_rowstate-column"></a><span data-ttu-id="89198-103">\_RowState-colonna</span><span class="sxs-lookup"><span data-stu-id="89198-103">\_RowState Column</span></span>

<span data-ttu-id="89198-104">Il nome di colonna riservato \_ RowState rappresenta lo stato non persistente associato a ogni riga della tabella in una tabella di database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="89198-104">The reserved column name \_RowState represents the non-persistent state associated with each table row in an installer database table.</span></span> <span data-ttu-id="89198-105">La pseudo-colonna è di tipo [Integer](integer.md)e il valore è costituito da un set di flag di bit.</span><span class="sxs-lookup"><span data-stu-id="89198-105">The pseudo-column is of type [Integer](integer.md), and the value consists of a set of bit flags.</span></span> <span data-ttu-id="89198-106">Tutti i bit sono leggibili, ma è possibile impostare solo UserInfo e BITS temporanei.</span><span class="sxs-lookup"><span data-stu-id="89198-106">All the bits are readable, but only the UserInfo and Temporary bits can be set.</span></span> <span data-ttu-id="89198-107">Questi dati sono disponibili solo se le tabelle sono bloccate o in uso, ovvero quando esiste una vista contenente le tabelle.</span><span class="sxs-lookup"><span data-stu-id="89198-107">This data is available only as long as the tables are locked or in use (that is, while a view containing the tables exists).</span></span> <span data-ttu-id="89198-108">La tabella seguente Mostra gli attributi che possono essere presenti in una riga.</span><span class="sxs-lookup"><span data-stu-id="89198-108">The following table shows the attributes a row can have.</span></span>



| <span data-ttu-id="89198-109">Nome</span><span class="sxs-lookup"><span data-stu-id="89198-109">Name</span></span>           | <span data-ttu-id="89198-110">Valore</span><span class="sxs-lookup"><span data-stu-id="89198-110">Value</span></span> | <span data-ttu-id="89198-111">Significato</span><span class="sxs-lookup"><span data-stu-id="89198-111">Meaning</span></span>                                                        |
|----------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="89198-112">iraUserInfo</span><span class="sxs-lookup"><span data-stu-id="89198-112">iraUserInfo</span></span>    | <span data-ttu-id="89198-113">0x01</span><span class="sxs-lookup"><span data-stu-id="89198-113">0x01</span></span>  | <span data-ttu-id="89198-114">L'attributo è per uso esterno.</span><span class="sxs-lookup"><span data-stu-id="89198-114">The attribute is for external use.</span></span> <span data-ttu-id="89198-115">Questo valore può essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="89198-115">This value can be updated.</span></span>  |
| <span data-ttu-id="89198-116">iraTemporary</span><span class="sxs-lookup"><span data-stu-id="89198-116">iraTemporary</span></span>   | <span data-ttu-id="89198-117">0x02</span><span class="sxs-lookup"><span data-stu-id="89198-117">0x02</span></span>  | <span data-ttu-id="89198-118">La riga non è persistente.</span><span class="sxs-lookup"><span data-stu-id="89198-118">The row is not persistent.</span></span> <span data-ttu-id="89198-119">Questo valore può essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="89198-119">This value can be updated.</span></span>          |
| <span data-ttu-id="89198-120">iraModified</span><span class="sxs-lookup"><span data-stu-id="89198-120">iraModified</span></span>    | <span data-ttu-id="89198-121">0x04</span><span class="sxs-lookup"><span data-stu-id="89198-121">0x04</span></span>  | <span data-ttu-id="89198-122">È stata aggiornata una riga.</span><span class="sxs-lookup"><span data-stu-id="89198-122">A row has been updated.</span></span>                                        |
| <span data-ttu-id="89198-123">iraInserted</span><span class="sxs-lookup"><span data-stu-id="89198-123">iraInserted</span></span>    | <span data-ttu-id="89198-124">0x08</span><span class="sxs-lookup"><span data-stu-id="89198-124">0x08</span></span>  | <span data-ttu-id="89198-125">È stata inserita una riga.</span><span class="sxs-lookup"><span data-stu-id="89198-125">A row has been inserted.</span></span>                                       |
| <span data-ttu-id="89198-126">iraMergeFailed</span><span class="sxs-lookup"><span data-stu-id="89198-126">iraMergeFailed</span></span> | <span data-ttu-id="89198-127">0x0F</span><span class="sxs-lookup"><span data-stu-id="89198-127">0x0F</span></span>  | <span data-ttu-id="89198-128">È stato effettuato un tentativo di Unione con dati non identici e non chiave.</span><span class="sxs-lookup"><span data-stu-id="89198-128">An attempt was made to merge with non-identical, non-key data.</span></span> |



 

<span data-ttu-id="89198-129">I bit da 6 a 8 sono riservati.</span><span class="sxs-lookup"><span data-stu-id="89198-129">Bits 6 through 8 are reserved.</span></span>

 

 



