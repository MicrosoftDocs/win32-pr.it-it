---
title: IDeviceIcon (Metodo ContentType)
description: Recupera il tipo di contenuto dell'icona.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- API di streaming multimediale del Metodo ContentType
- API di streaming multimediale del Metodo ContentType, interfaccia IDeviceIcon
- API di streaming multimediale dell'interfaccia IDeviceIcon, Metodo ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872366"
---
# <a name="ideviceiconcontenttype-method"></a><span data-ttu-id="f171d-106">Metodo IDeviceIcon:: ContentType</span><span class="sxs-lookup"><span data-stu-id="f171d-106">IDeviceIcon::ContentType method</span></span>

<span data-ttu-id="f171d-107">Recupera il tipo di contenuto dell'icona.</span><span class="sxs-lookup"><span data-stu-id="f171d-107">Retrieves the content type of the icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="f171d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f171d-108">Syntax</span></span>


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="f171d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f171d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f171d-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f171d-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f171d-111">Riceve un puntatore al tipo di contenuto dell'icona.</span><span class="sxs-lookup"><span data-stu-id="f171d-111">Receives a pointer to the content type of the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f171d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f171d-112">Return value</span></span>

<span data-ttu-id="f171d-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f171d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f171d-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f171d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f171d-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f171d-115">Return code</span></span>                                                                          | <span data-ttu-id="f171d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f171d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f171d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f171d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f171d-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f171d-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f171d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f171d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f171d-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="f171d-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

