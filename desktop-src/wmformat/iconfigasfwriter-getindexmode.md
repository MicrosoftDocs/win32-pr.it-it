---
title: Metodo IConfigAsfWriter GetIndexMode
description: Il metodo GetIndexMode recupera la modalità di indice temporale corrente.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Metodo GetIndexMode Windows Media Format
- Metodo GetIndexMode Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo GetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399280"
---
# <a name="iconfigasfwritergetindexmode-method"></a><span data-ttu-id="461d6-106">Metodo IConfigAsfWriter:: GetIndexMode</span><span class="sxs-lookup"><span data-stu-id="461d6-106">IConfigAsfWriter::GetIndexMode method</span></span>

<span data-ttu-id="461d6-107">Il metodo **GetIndexMode** recupera la modalità di indice temporale corrente.</span><span class="sxs-lookup"><span data-stu-id="461d6-107">The **GetIndexMode** method retrieves the current temporal index mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="461d6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="461d6-108">Syntax</span></span>


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="461d6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="461d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="461d6-110">*pbIndexFile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="461d6-110">*pbIndexFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="461d6-111">Puntatore a una variabile di tipo **bool** che riceve l'impostazione della modalità di indice temporale.</span><span class="sxs-lookup"><span data-stu-id="461d6-111">Pointer to a variable of type **BOOL** that receives the temporal index mode setting.</span></span> <span data-ttu-id="461d6-112">Il valore **true** indica che il writer ASF WM è configurato per la scrittura di file indicizzati temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="461d6-112">A value of **TRUE** indicates that the WM ASF Writer is configured to write temporally indexed files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="461d6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="461d6-113">Return value</span></span>

<span data-ttu-id="461d6-114">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="461d6-114">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="461d6-115">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="461d6-115">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="461d6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="461d6-116">Remarks</span></span>

<span data-ttu-id="461d6-117">Usare questo metodo per determinare se il [writer ASF WM](wm-asf-writer-filter.md) è attualmente configurato per la scrittura di file ASF indicizzati temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="461d6-117">Use this method to determine whether the [WM ASF Writer](wm-asf-writer-filter.md) is currently configured to write temporally indexed ASF files.</span></span> <span data-ttu-id="461d6-118">Per ulteriori informazioni sui file indicizzati e indicizzati temporalmente, vedere la sezione Note per [**IConfigAsfWriter:: SetIndexMode**](iconfigasfwriter-setindexmode.md).</span><span class="sxs-lookup"><span data-stu-id="461d6-118">For more information on temporally indexed and frame-indexed files, see the Remarks for [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="461d6-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="461d6-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="461d6-120">[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="461d6-120">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 