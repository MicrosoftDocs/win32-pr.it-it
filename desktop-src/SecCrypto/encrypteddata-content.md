---
description: Imposta o Recupera il contenuto da crittografare o decrittografare.
ms.assetid: fdab0f19-c69e-443b-b4b3-079d23028921
title: Proprietà EncryptedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b873d40ed04270defe04fd59f0ce00a0f84040a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324903"
---
# <a name="encrypteddatacontent-property"></a><span data-ttu-id="fd7ba-103">Proprietà EncryptedData. Content</span><span class="sxs-lookup"><span data-stu-id="fd7ba-103">EncryptedData.Content property</span></span>

<span data-ttu-id="fd7ba-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd7ba-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fd7ba-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="fd7ba-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="fd7ba-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd7ba-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="fd7ba-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="fd7ba-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="fd7ba-108">La proprietà **Content** imposta o Recupera il contenuto da crittografare o decrittografare.</span><span class="sxs-lookup"><span data-stu-id="fd7ba-108">The **Content** property sets or retrieves the content to be encrypted or decrypted.</span></span> <span data-ttu-id="fd7ba-109">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="fd7ba-109">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7ba-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd7ba-110">Syntax</span></span>


```VB
EncryptedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="fd7ba-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fd7ba-111">Property value</span></span>

<span data-ttu-id="fd7ba-112">Contenuto da crittografare o decrittografare.</span><span class="sxs-lookup"><span data-stu-id="fd7ba-112">The content to be encrypted or decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7ba-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd7ba-113">Requirements</span></span>



| <span data-ttu-id="fd7ba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7ba-114">Requirement</span></span> | <span data-ttu-id="fd7ba-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7ba-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7ba-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fd7ba-116">End of client support</span></span><br/> | <span data-ttu-id="fd7ba-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd7ba-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fd7ba-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fd7ba-118">End of server support</span></span><br/> | <span data-ttu-id="fd7ba-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd7ba-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fd7ba-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fd7ba-120">Redistributable</span></span><br/>       | <span data-ttu-id="fd7ba-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fd7ba-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fd7ba-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fd7ba-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fd7ba-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ba-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd7ba-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd7ba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7ba-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="fd7ba-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
