---
description: Ottiene la chiave utilizzata per crittografare i messaggi in uscita protetti dal token.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'Metodo IUpdateEndpointAuthToken:: SigningKey (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049541"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a><span data-ttu-id="a1f7c-103">Metodo IUpdateEndpointAuthToken:: SigningKey</span><span class="sxs-lookup"><span data-stu-id="a1f7c-103">IUpdateEndpointAuthToken::SigningKey method</span></span>

<span data-ttu-id="a1f7c-104">Ottiene la chiave utilizzata per crittografare i messaggi in uscita protetti dal token.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-104">Gets the key that is used to encrypt the outgoing messages that the token protects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f7c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1f7c-105">Syntax</span></span>


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a><span data-ttu-id="a1f7c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1f7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f7c-107">*pbKey* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a1f7c-107">*pbKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f7c-108">Chiave utilizzata per crittografare il messaggio in uscita.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-108">Key used to encrypt outgoing message.</span></span>

</dd> <dt>

<span data-ttu-id="a1f7c-109">*pcbKeySize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a1f7c-109">*pcbKeySize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f7c-110">Dimensione della chiave a cui fa riferimento il rndSrc *pbkey* .</span><span class="sxs-lookup"><span data-stu-id="a1f7c-110">Size of the key referenced by the *pbkey* paremeter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f7c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1f7c-111">Return value</span></span>

<span data-ttu-id="a1f7c-112">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-112">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="a1f7c-113">In caso contrario, restituisce un codice di errore COM o Windows.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-113">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f7c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1f7c-114">Requirements</span></span>



| <span data-ttu-id="a1f7c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1f7c-115">Requirement</span></span> | <span data-ttu-id="a1f7c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a1f7c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f7c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1f7c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a1f7c-118">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a1f7c-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a1f7c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1f7c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a1f7c-120">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a1f7c-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a1f7c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1f7c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1f7c-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1f7c-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1f7c-123">IDL</span><span class="sxs-lookup"><span data-stu-id="a1f7c-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a1f7c-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1f7c-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="a1f7c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1f7c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1f7c-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1f7c-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="a1f7c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a1f7c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1f7c-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1f7c-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f7c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1f7c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f7c-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="a1f7c-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




