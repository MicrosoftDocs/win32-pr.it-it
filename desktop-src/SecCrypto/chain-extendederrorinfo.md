---
description: Restituisce una stringa che contiene informazioni aggiuntive sull'errore relative alla voce indicizzata.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'Metodo IChain2:: ExtendedErrorInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329612"
---
# <a name="ichain2extendederrorinfo-method"></a><span data-ttu-id="ff301-103">Metodo IChain2:: ExtendedErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ff301-103">IChain2::ExtendedErrorInfo method</span></span>

<span data-ttu-id="ff301-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff301-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ff301-105">Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ff301-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ff301-106">Il metodo **ExtendedErrorInfo** restituisce una stringa che contiene informazioni aggiuntive sull'errore relative alla voce indicizzata.</span><span class="sxs-lookup"><span data-stu-id="ff301-106">The **ExtendedErrorInfo** method returns a string that contains additional error information about the indexed entry.</span></span>

<span data-ttu-id="ff301-107">Questo metodo è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="ff301-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff301-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff301-108">Syntax</span></span>


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ff301-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff301-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff301-110">*Indice* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ff301-110">*Index* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ff301-111">Oggetto **Long** che rappresenta l'indice della voce.</span><span class="sxs-lookup"><span data-stu-id="ff301-111">A **Long** representing the index of the entry.</span></span> <span data-ttu-id="ff301-112">Il valore predefinito è 1, che restituisce informazioni sull'errore per il certificato finale nella catena.</span><span class="sxs-lookup"><span data-stu-id="ff301-112">The default value is 1, which returns error information for the end certificate in the chain.</span></span> <span data-ttu-id="ff301-113">**Certificates. Count** restituisce informazioni sul certificato radice della catena.</span><span class="sxs-lookup"><span data-stu-id="ff301-113">**Certificates.Count** returns information about the root certificate of the chain.</span></span> <span data-ttu-id="ff301-114">0 restituisce informazioni estese sull'errore per l'intera catena.</span><span class="sxs-lookup"><span data-stu-id="ff301-114">0 returns extended error information for the entire chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff301-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff301-115">Return value</span></span>

<span data-ttu-id="ff301-116">Stringa che contiene le informazioni estese sull'errore.</span><span class="sxs-lookup"><span data-stu-id="ff301-116">A string that contains the extended error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff301-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff301-117">Requirements</span></span>



| <span data-ttu-id="ff301-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff301-118">Requirement</span></span> | <span data-ttu-id="ff301-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ff301-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff301-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ff301-120">End of client support</span></span><br/> | <span data-ttu-id="ff301-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff301-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ff301-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ff301-122">End of server support</span></span><br/> | <span data-ttu-id="ff301-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff301-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ff301-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ff301-124">Redistributable</span></span><br/>       | <span data-ttu-id="ff301-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff301-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ff301-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ff301-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ff301-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff301-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff301-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff301-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff301-129">**Catena**</span><span class="sxs-lookup"><span data-stu-id="ff301-129">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
