---
description: Rimuove tutti gli oggetti certificato da una raccolta di destinatari.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Metodo Recipients. Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326354"
---
# <a name="recipientsclear-method"></a><span data-ttu-id="49126-103">Metodo Recipients. Clear</span><span class="sxs-lookup"><span data-stu-id="49126-103">Recipients.Clear method</span></span>

<span data-ttu-id="49126-104">\[Il metodo **Clear** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="49126-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="49126-105">Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="49126-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="49126-106">Il metodo **Clear** rimuove tutti gli oggetti [**certificato**](certificate.md) da una raccolta [**Recipients**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="49126-106">The **Clear** method removes all [**Certificate**](certificate.md) objects from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="49126-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49126-107">Syntax</span></span>


```VB
Recipients.Clear()
```



## <a name="parameters"></a><span data-ttu-id="49126-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="49126-108">Parameters</span></span>

<span data-ttu-id="49126-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="49126-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49126-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49126-110">Return value</span></span>

<span data-ttu-id="49126-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="49126-111">This method does not return a value.</span></span> <span data-ttu-id="49126-112">Un'applicazione che usa questo metodo deve contenere codice per gestire un'eccezione generata da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="49126-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="49126-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49126-113">Requirements</span></span>



| <span data-ttu-id="49126-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="49126-114">Requirement</span></span> | <span data-ttu-id="49126-115">Valore</span><span class="sxs-lookup"><span data-stu-id="49126-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49126-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="49126-116">Redistributable</span></span><br/> | <span data-ttu-id="49126-117">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="49126-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="49126-118">DLL</span><span class="sxs-lookup"><span data-stu-id="49126-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="49126-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49126-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49126-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49126-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49126-121">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="49126-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="49126-122">**Destinatari**</span><span class="sxs-lookup"><span data-stu-id="49126-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
