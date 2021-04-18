---
description: Recupera l'algoritmo per i dati crittografati.
ms.assetid: 37bebe69-3c62-44c4-a5e5-c8cdbf087fa4
title: Proprietà EncryptedData. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cd73fbda4a5f77706ac2253782768e8487b8cbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330023"
---
# <a name="encrypteddataalgorithm-property"></a><span data-ttu-id="85c21-103">Proprietà EncryptedData. Algorithm</span><span class="sxs-lookup"><span data-stu-id="85c21-103">EncryptedData.Algorithm property</span></span>

<span data-ttu-id="85c21-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85c21-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="85c21-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="85c21-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="85c21-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="85c21-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="85c21-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="85c21-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="85c21-108">La proprietà **Algorithm** recupera l'algoritmo per i dati crittografati.</span><span class="sxs-lookup"><span data-stu-id="85c21-108">The **Algorithm** property retrieves the algorithm for the encrypted data.</span></span>

<span data-ttu-id="85c21-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="85c21-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c21-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85c21-110">Syntax</span></span>


```VB
EncryptedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="85c21-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="85c21-111">Property value</span></span>

<span data-ttu-id="85c21-112">Oggetto [**algoritmo**](algorithm.md) che rappresenta l'algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="85c21-112">An [**Algorithm**](algorithm.md) object that represents the encryption algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c21-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85c21-113">Requirements</span></span>



| <span data-ttu-id="85c21-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c21-114">Requirement</span></span> | <span data-ttu-id="85c21-115">Valore</span><span class="sxs-lookup"><span data-stu-id="85c21-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85c21-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="85c21-116">End of client support</span></span><br/> | <span data-ttu-id="85c21-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85c21-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="85c21-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="85c21-118">End of server support</span></span><br/> | <span data-ttu-id="85c21-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85c21-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="85c21-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="85c21-120">Redistributable</span></span><br/>       | <span data-ttu-id="85c21-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="85c21-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="85c21-122">DLL</span><span class="sxs-lookup"><span data-stu-id="85c21-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="85c21-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85c21-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c21-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85c21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c21-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="85c21-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
