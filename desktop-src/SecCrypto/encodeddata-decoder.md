---
description: Ottiene un oggetto decodificatore, se ne esiste uno.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: Metodo EncodedData. decoder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331423"
---
# <a name="encodeddatadecoder-method"></a><span data-ttu-id="16c79-103">Metodo EncodedData. decoder</span><span class="sxs-lookup"><span data-stu-id="16c79-103">EncodedData.Decoder method</span></span>

<span data-ttu-id="16c79-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16c79-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="16c79-105">Usare invece la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="16c79-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="16c79-106">Il metodo **decodificatore** ottiene un oggetto decodificatore, se ne esiste uno.</span><span class="sxs-lookup"><span data-stu-id="16c79-106">The **Decoder** method obtains a decoder object, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c79-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16c79-107">Syntax</span></span>


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a><span data-ttu-id="16c79-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="16c79-108">Parameters</span></span>

<span data-ttu-id="16c79-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="16c79-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="16c79-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="16c79-110">Remarks</span></span>

<span data-ttu-id="16c79-111">Se i dati codificati non dispongono di un oggetto Decoder, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="16c79-111">If the encoded data does not have a decoder object, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c79-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16c79-112">Requirements</span></span>



| <span data-ttu-id="16c79-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c79-113">Requirement</span></span> | <span data-ttu-id="16c79-114">Valore</span><span class="sxs-lookup"><span data-stu-id="16c79-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16c79-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="16c79-115">End of client support</span></span><br/> | <span data-ttu-id="16c79-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16c79-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="16c79-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="16c79-117">End of server support</span></span><br/> | <span data-ttu-id="16c79-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16c79-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="16c79-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="16c79-119">Redistributable</span></span><br/>       | <span data-ttu-id="16c79-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="16c79-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="16c79-121">DLL</span><span class="sxs-lookup"><span data-stu-id="16c79-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="16c79-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16c79-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
