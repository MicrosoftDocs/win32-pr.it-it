---
title: Metodo flusso IDeviceIcon
description: Recupera l'icona come flusso.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- API flusso multimediale per il metodo Stream
- API flusso multimediale del metodo di flusso, interfaccia IDeviceIcon
- API di streaming multimediale dell'interfaccia IDeviceIcon, metodo Stream
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337407"
---
# <a name="ideviceiconstream-method"></a><span data-ttu-id="416f7-106">Metodo IDeviceIcon:: Stream</span><span class="sxs-lookup"><span data-stu-id="416f7-106">IDeviceIcon::Stream method</span></span>

<span data-ttu-id="416f7-107">Recupera l'icona come flusso.</span><span class="sxs-lookup"><span data-stu-id="416f7-107">Retrieves the icon as a stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="416f7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="416f7-108">Syntax</span></span>


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a><span data-ttu-id="416f7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="416f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="416f7-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="416f7-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="416f7-111">Riceve un riferimento a un [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) che può essere usato per recuperare i dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="416f7-111">Receives a reference to a [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) that can be used to retrieve the image data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="416f7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="416f7-112">Return value</span></span>

<span data-ttu-id="416f7-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="416f7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="416f7-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="416f7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="416f7-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="416f7-115">Return code</span></span>                                                                          | <span data-ttu-id="416f7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="416f7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="416f7-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="416f7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="416f7-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="416f7-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="416f7-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="416f7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416f7-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="416f7-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

