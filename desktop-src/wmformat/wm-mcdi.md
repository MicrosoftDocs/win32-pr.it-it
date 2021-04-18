---
title: WM/MCDI
description: L'attributo WM/MCDI contiene l'identificatore del CD musicale. Si tratta di un dump binario del sommario del CD usato per identificare in modo univoco il CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato di Windows Media WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299222"
---
# <a name="wmmcdi"></a><span data-ttu-id="20bdb-105">WM/MCDI</span><span class="sxs-lookup"><span data-stu-id="20bdb-105">WM/MCDI</span></span>

<span data-ttu-id="20bdb-106">L'attributo **WM/MCDI** contiene l'identificatore del CD musicale.</span><span class="sxs-lookup"><span data-stu-id="20bdb-106">The **WM/MCDI** attribute contains the music CD identifier.</span></span> <span data-ttu-id="20bdb-107">Si tratta di un dump binario del sommario del CD usato per identificare in modo univoco il CD.</span><span class="sxs-lookup"><span data-stu-id="20bdb-107">This is a binary dump of the table of contents from the CD that is used to uniquely identify the CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="20bdb-108">Costante globale</span><span class="sxs-lookup"><span data-stu-id="20bdb-108">Global Constant</span></span>

<span data-ttu-id="20bdb-109">g \_ wszWMMCDI</span><span class="sxs-lookup"><span data-stu-id="20bdb-109">g\_wszWMMCDI</span></span>

## <a name="data-type"></a><span data-ttu-id="20bdb-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="20bdb-110">Data Type</span></span>

<span data-ttu-id="20bdb-111">**\_binario di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="20bdb-111">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="20bdb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="20bdb-112">Remarks</span></span>

<span data-ttu-id="20bdb-113">Questo attributo è compatibile con il frame ID3, MCDI.</span><span class="sxs-lookup"><span data-stu-id="20bdb-113">This attribute is compatible with the ID3 frame, MCDI.</span></span> <span data-ttu-id="20bdb-114">Per la specifica ID3 per il frame MCDI è necessario che esista un solo frame per ogni file e che esista un frame TRCK valido.</span><span class="sxs-lookup"><span data-stu-id="20bdb-114">The ID3 specification for the MCDI frame requires that only one such frame exist per file and that a valid TRCK frame exist.</span></span> <span data-ttu-id="20bdb-115">L'editor dei metadati non esegue alcuna convalida per queste regole.</span><span class="sxs-lookup"><span data-stu-id="20bdb-115">The metadata editor does not perform any validation for these rules.</span></span> <span data-ttu-id="20bdb-116">Inoltre, le dimensioni di WM/MCDI non sono limitate a 804 byte, così come il frame ID3 MCDI.</span><span class="sxs-lookup"><span data-stu-id="20bdb-116">Also, the size of WM/MCDI is not limited to 804 bytes, as is the MCDI ID3 frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="20bdb-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20bdb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bdb-118">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="20bdb-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




