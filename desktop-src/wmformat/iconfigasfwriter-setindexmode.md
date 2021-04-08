---
title: Metodo IConfigAsfWriter SetIndexMode
description: Il metodo SetIndexMode consente all'applicazione di controllare se il file verrà indicizzato temporaneamente.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Metodo SetIndexMode Windows Media Format
- Metodo SetIndexMode Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo SetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046790"
---
# <a name="iconfigasfwritersetindexmode-method"></a><span data-ttu-id="a48a1-106">Metodo IConfigAsfWriter:: SetIndexMode</span><span class="sxs-lookup"><span data-stu-id="a48a1-106">IConfigAsfWriter::SetIndexMode method</span></span>

<span data-ttu-id="a48a1-107">Il metodo **SetIndexMode** consente all'applicazione di controllare se il file verrà indicizzato temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="a48a1-107">The **SetIndexMode** method enables the application to control whether the file will be temporally indexed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a48a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a48a1-108">Syntax</span></span>


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="a48a1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a48a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a48a1-110">*bIndexFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a48a1-110">*bIndexFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a48a1-111">Variabile di tipo **bool**; **True** indica che il file verrà indicizzato temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="a48a1-111">Variable of type **BOOL**; **TRUE** specifies that the file will be temporally indexed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a48a1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a48a1-112">Return value</span></span>

<span data-ttu-id="a48a1-113">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a48a1-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="a48a1-114">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a48a1-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a48a1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a48a1-115">Remarks</span></span>

<span data-ttu-id="a48a1-116">Per impostazione predefinita, il [writer ASF WM](wm-asf-writer-filter.md) crea file ASF indicizzati temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="a48a1-116">By default, the [WM ASF Writer](wm-asf-writer-filter.md) creates temporally indexed ASF files.</span></span> <span data-ttu-id="a48a1-117">Esegue l'indicizzazione quando il grafico si arresta.</span><span class="sxs-lookup"><span data-stu-id="a48a1-117">It performs the indexing when the graph stops.</span></span> <span data-ttu-id="a48a1-118">È possibile disabilitare questo comportamento se si vuole eseguire l'indicizzazione basata su frame come passaggio di post-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a48a1-118">You can disable this behavior if you want to do your own frame-based indexing as a post-processing step.</span></span> <span data-ttu-id="a48a1-119">Per creare un file indicizzato con frame, chiamare **SetIndexMode**(false), creare il file e quindi usare direttamente i metodi Windows Media Format SDK per creare un indice basato su frame per il file.</span><span class="sxs-lookup"><span data-stu-id="a48a1-119">To create a frame-indexed file, call **SetIndexMode**(FALSE), create the file, and then use the Windows Media Format SDK methods directly to create a frame-based index for the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="a48a1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a48a1-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="a48a1-121">[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a48a1-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 