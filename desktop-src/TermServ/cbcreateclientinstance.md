---
title: Funzione CBCreateClientInstance (Cbclient. h)
description: Crea un'istanza del client RPC di Connessione Desktop remoto broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto funzione CBCreateClientInstance
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333646"
---
# <a name="cbcreateclientinstance-function"></a><span data-ttu-id="a4b14-104">CBCreateClientInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="a4b14-104">CBCreateClientInstance function</span></span>

<span data-ttu-id="a4b14-105">Crea un'istanza del client RPC di Connessione Desktop remoto broker.</span><span class="sxs-lookup"><span data-stu-id="a4b14-105">Creates an instance of the Remote Desktop Connection Broker RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b14-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4b14-106">Syntax</span></span>


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a><span data-ttu-id="a4b14-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4b14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b14-108">*Versione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a4b14-108">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b14-109">Specifica la versione dell'interfaccia client di Connessione Desktop remoto broker richiesta.</span><span class="sxs-lookup"><span data-stu-id="a4b14-109">Specifies the version of the Remote Desktop Connection Broker client interface being requested.</span></span> <span data-ttu-id="a4b14-110">Deve corrispondere al valore seguente.</span><span class="sxs-lookup"><span data-stu-id="a4b14-110">This must be the following value.</span></span>

<dt>

<span data-ttu-id="a4b14-111">1</span><span class="sxs-lookup"><span data-stu-id="a4b14-111">1</span></span>
</dt> <dd>

<span data-ttu-id="a4b14-112">Versione 1 del client di Connessione Desktop remoto broker.</span><span class="sxs-lookup"><span data-stu-id="a4b14-112">Version 1 of the Remote Desktop Connection Broker client.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a4b14-113">*ppCbClient* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a4b14-113">*ppCbClient* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b14-114">Indirizzo di un puntatore a interfaccia [**IConnectionBrokerClient**](iconnectionbrokerclient.md) che riceve l'oggetto client di connessione Desktop remoto broker.</span><span class="sxs-lookup"><span data-stu-id="a4b14-114">The address of an [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface pointer that receives the Remote Desktop Connection Broker client object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b14-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4b14-115">Return value</span></span>

<span data-ttu-id="a4b14-116">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a4b14-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4b14-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4b14-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b14-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4b14-118">Requirements</span></span>



| <span data-ttu-id="a4b14-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b14-119">Requirement</span></span> | <span data-ttu-id="a4b14-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a4b14-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b14-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4b14-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a4b14-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b14-122"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4b14-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="a4b14-123">Library</span></span><br/> | <dl> <span data-ttu-id="a4b14-124"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4b14-124"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="a4b14-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b14-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4b14-126"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b14-126"><dt>Cbclient.dll</dt></span></span> </dl> |



 

 





