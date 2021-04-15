---
title: ODJ_BLOB
description: Definizione di ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104474591"
---
# <a name="odj_blob-structure"></a><span data-ttu-id="bce1f-103">Struttura ODJ_BLOB</span><span class="sxs-lookup"><span data-stu-id="bce1f-103">ODJ_BLOB structure</span></span>

<span data-ttu-id="bce1f-104">Specifica una struttura che contiene una struttura di ODJ_WIN7BLOB serializzata o una struttura OP_PACKAGE serializzata.</span><span class="sxs-lookup"><span data-stu-id="bce1f-104">Specifies a structure containing either a serialized ODJ_WIN7BLOB structure or a serialized OP_PACKAGE structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce1f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bce1f-105">Syntax</span></span>

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a><span data-ttu-id="bce1f-106">Members</span><span class="sxs-lookup"><span data-stu-id="bce1f-106">Members</span></span>

### <a name="ulodjformat"></a><span data-ttu-id="bce1f-107">ulODJFormat</span><span class="sxs-lookup"><span data-stu-id="bce1f-107">ulODJFormat</span></span>

<span data-ttu-id="bce1f-108">Specifica la versione logica della struttura e deve essere impostata su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bce1f-108">Specifies the logical version of the structure and must be set to one of the following values:</span></span>

|<span data-ttu-id="bce1f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="bce1f-109">Value</span></span>|<span data-ttu-id="bce1f-110">Significato</span><span class="sxs-lookup"><span data-stu-id="bce1f-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="bce1f-111">ODJ_WIN7_FORMAT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="bce1f-111">ODJ_WIN7_FORMAT (0x00000001)</span></span>|<span data-ttu-id="bce1f-112">I byte contenuti in pBlob devono contenere una struttura ODJ_WIN7_BLOB serializzata.</span><span class="sxs-lookup"><span data-stu-id="bce1f-112">The bytes contained in pBlob must contain a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="bce1f-113">ODJ_WIN8_FORMAT (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="bce1f-113">ODJ_WIN8_FORMAT (0x00000002)</span></span>|<span data-ttu-id="bce1f-114">I byte contenuti in pBlob devono contenere una struttura OP_PACKAGE serializzata.</span><span class="sxs-lookup"><span data-stu-id="bce1f-114">The bytes contained in pBlob must contain a serialized OP_PACKAGE structure.</span></span>|

### <a name="cbblob"></a><span data-ttu-id="bce1f-115">cbBlob</span><span class="sxs-lookup"><span data-stu-id="bce1f-115">cbBlob</span></span>

<span data-ttu-id="bce1f-116">Deve essere impostato sul numero di byte nella matrice pBlob.</span><span class="sxs-lookup"><span data-stu-id="bce1f-116">This must be set to the number of bytes in the pBlob array.</span></span>

### <a name="pblob"></a><span data-ttu-id="bce1f-117">pBlob</span><span class="sxs-lookup"><span data-stu-id="bce1f-117">pBlob</span></span>

<span data-ttu-id="bce1f-118">Punta a un buffer di byte contenente una struttura serializzata come specificato da ulODJFormat sopra.</span><span class="sxs-lookup"><span data-stu-id="bce1f-118">Points to a byte buffer containing a serialized structure as specified by ulODJFormat above.</span></span>

## <a name="see-also"></a><span data-ttu-id="bce1f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bce1f-119">See also</span></span>

[<span data-ttu-id="bce1f-120">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="bce1f-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

