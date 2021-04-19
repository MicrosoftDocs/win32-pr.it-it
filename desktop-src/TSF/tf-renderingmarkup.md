---
title: Struttura TF_RENDERINGMARKUP
description: La \_ struttura della struttura TF RENDERINGMARKUP contiene un intervallo e le informazioni sugli attributi di visualizzazione.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- Framework servizi di testo struttura TF_RENDERINGMARKUP
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299067"
---
# <a name="tf_renderingmarkup-structure"></a><span data-ttu-id="4d7bc-104">\_Struttura RENDERINGMARKUP TF</span><span class="sxs-lookup"><span data-stu-id="4d7bc-104">TF\_RENDERINGMARKUP structure</span></span>

<span data-ttu-id="4d7bc-105">La struttura della struttura [**tf \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contiene un intervallo e le informazioni sugli attributi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4d7bc-105">The [**TF\_RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) structure structure contains a range and the display attribute information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7bc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d7bc-106">Syntax</span></span>


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a><span data-ttu-id="4d7bc-107">Members</span><span class="sxs-lookup"><span data-stu-id="4d7bc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d7bc-108">**pRange**</span><span class="sxs-lookup"><span data-stu-id="4d7bc-108">**pRange**</span></span>
</dt> <dd>

<span data-ttu-id="4d7bc-109">Puntatore a un'interfaccia [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) .</span><span class="sxs-lookup"><span data-stu-id="4d7bc-109">A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface.</span></span>

</dd> <dt>

<span data-ttu-id="4d7bc-110">**tfDisplayAttr**</span><span class="sxs-lookup"><span data-stu-id="4d7bc-110">**tfDisplayAttr**</span></span>
</dt> <dd>

<span data-ttu-id="4d7bc-111">Visualizzare le informazioni sugli attributi.</span><span class="sxs-lookup"><span data-stu-id="4d7bc-111">Display attribute information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d7bc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d7bc-112">Remarks</span></span>

<span data-ttu-id="4d7bc-113">Questa struttura non è attualmente presente nei file di intestazione pubblici.</span><span class="sxs-lookup"><span data-stu-id="4d7bc-113">This structure is not currently in the public header files.</span></span> <span data-ttu-id="4d7bc-114">Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="4d7bc-114">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 




