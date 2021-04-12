---
title: WMCreateStreamForURL (funzione)
description: La funzione WMCreateStreamForURL viene implementata dall'applicazione per creare un oggetto IStream COM per un determinato URL.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Formato Windows Media della funzione WMCreateStreamForURL
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397783"
---
# <a name="wmcreatestreamforurl-function"></a><span data-ttu-id="3aadb-104">WMCreateStreamForURL (funzione)</span><span class="sxs-lookup"><span data-stu-id="3aadb-104">WMCreateStreamForURL function</span></span>

<span data-ttu-id="3aadb-105">La funzione **WMCreateStreamForURL** viene implementata dall'applicazione per creare un oggetto **IStream** com per un determinato URL.</span><span class="sxs-lookup"><span data-stu-id="3aadb-105">The **WMCreateStreamForURL** function is implemented by the application to create a COM **IStream** object for a given URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aadb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3aadb-106">Syntax</span></span>


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a><span data-ttu-id="3aadb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3aadb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aadb-108">*pwszURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3aadb-108">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aadb-109">Puntatore a una stringa di caratteri wide contenente l'URL.</span><span class="sxs-lookup"><span data-stu-id="3aadb-109">Pointer to a wide-character string containing the URL.</span></span>

</dd> <dt>

<span data-ttu-id="3aadb-110">*pfCorrectSource* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3aadb-110">*pfCorrectSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aadb-111">Puntatore a un flag, true impedirà all'SDK di provare altri plug-in di origine per questo URL.</span><span class="sxs-lookup"><span data-stu-id="3aadb-111">Pointer to a flag, true will prevent the SDK from trying other source plug-ins for this URL.</span></span>

</dd> <dt>

<span data-ttu-id="3aadb-112">*ppStream* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3aadb-112">*ppStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aadb-113">Puntatore a un puntatore all'oggetto **IStream** creato dal metodo.</span><span class="sxs-lookup"><span data-stu-id="3aadb-113">Pointer to a pointer to the **IStream** object created by the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aadb-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3aadb-114">Return value</span></span>

<span data-ttu-id="3aadb-115">Se la funzione ha esito positivo, deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3aadb-115">If the function succeeds, it must return S\_OK.</span></span> <span data-ttu-id="3aadb-116">Se ha esito negativo, deve restituire un codice di errore **HRESULT** appropriato e \* *ppStream* deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="3aadb-116">If it fails, it must return an appropriate **HRESULT** error code, and \**ppStream* should be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="3aadb-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3aadb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aadb-118">**Plug-in di origine**</span><span class="sxs-lookup"><span data-stu-id="3aadb-118">**Source Plug-ins**</span></span>](source-plug-ins.md)
</dt> </dl>

 

 




