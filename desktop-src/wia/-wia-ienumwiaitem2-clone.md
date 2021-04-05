---
description: Crea un'istanza aggiuntiva dell'interfaccia IEnumWiaItem2 e restituisce un puntatore.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'Metodo IEnumWiaItem2:: Clone (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752871"
---
# <a name="ienumwiaitem2clone-method"></a><span data-ttu-id="4645d-103">Metodo IEnumWiaItem2:: Clone</span><span class="sxs-lookup"><span data-stu-id="4645d-103">IEnumWiaItem2::Clone method</span></span>

<span data-ttu-id="4645d-104">Crea un'istanza aggiuntiva dell'interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) e restituisce un puntatore.</span><span class="sxs-lookup"><span data-stu-id="4645d-104">Creates an additional instance of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface and sends back a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4645d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4645d-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="4645d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4645d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4645d-107">*ppIEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4645d-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4645d-108">Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4645d-108">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="4645d-109">Riceve l'indirizzo dell'istanza dell'interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) creata da **IEnumWiaItem2:: Clone** .</span><span class="sxs-lookup"><span data-stu-id="4645d-109">Receives the address of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface instance that **IEnumWiaItem2::Clone** creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4645d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4645d-110">Return value</span></span>

<span data-ttu-id="4645d-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4645d-111">Type: **HRESULT**</span></span>

<span data-ttu-id="4645d-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4645d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4645d-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4645d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4645d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4645d-114">Remarks</span></span>

<span data-ttu-id="4645d-115">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="4645d-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4645d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4645d-116">Requirements</span></span>



| <span data-ttu-id="4645d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4645d-117">Requirement</span></span> | <span data-ttu-id="4645d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4645d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4645d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4645d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4645d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4645d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4645d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4645d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4645d-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4645d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4645d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4645d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4645d-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4645d-124"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4645d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="4645d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4645d-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4645d-126"><dt>Wia.idl</dt></span></span> </dl> |



 

 
