---
description: Imposta o Recupera il contenuto di testo non crittografato di un messaggio da racchiudere. Si tratta della proprietà predefinita.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Proprietà EnvelopedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327898"
---
# <a name="envelopeddatacontent-property"></a><span data-ttu-id="7b313-104">Proprietà EnvelopedData. Content</span><span class="sxs-lookup"><span data-stu-id="7b313-104">EnvelopedData.Content property</span></span>

<span data-ttu-id="7b313-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b313-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7b313-106">Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="7b313-106">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7b313-107">La proprietà **Content** imposta o Recupera il contenuto di testo non crittografato di un messaggio da racchiudere.</span><span class="sxs-lookup"><span data-stu-id="7b313-107">The **Content** property sets or retrieves the plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="7b313-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="7b313-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b313-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b313-109">Syntax</span></span>


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="7b313-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7b313-110">Property value</span></span>

<span data-ttu-id="7b313-111">Contenuto di testo non crittografato di un messaggio da racchiudere.</span><span class="sxs-lookup"><span data-stu-id="7b313-111">The plaintext content of a message to be enveloped.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b313-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b313-112">Remarks</span></span>

<span data-ttu-id="7b313-113">L'impostazione di questa proprietà deve essere eseguita prima che venga chiamato il metodo [**Encrypt**](envelopeddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="7b313-113">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span> <span data-ttu-id="7b313-114">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e qualsiasi contenuto crittografato nell'oggetto viene perso.</span><span class="sxs-lookup"><span data-stu-id="7b313-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b313-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b313-115">Requirements</span></span>



| <span data-ttu-id="7b313-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b313-116">Requirement</span></span> | <span data-ttu-id="7b313-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7b313-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b313-118">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7b313-118">End of client support</span></span><br/> | <span data-ttu-id="7b313-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b313-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b313-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7b313-120">End of server support</span></span><br/> | <span data-ttu-id="7b313-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b313-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b313-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7b313-122">Redistributable</span></span><br/>       | <span data-ttu-id="7b313-123">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b313-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7b313-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7b313-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7b313-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b313-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b313-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b313-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b313-127">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="7b313-127">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
