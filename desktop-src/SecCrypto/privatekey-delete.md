---
description: Elimina il contenitore di chiavi private a cui fa riferimento l'oggetto PrivateKey.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: Metodo PrivateKey. Delete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325461"
---
# <a name="privatekeydelete-method"></a><span data-ttu-id="6b422-103">Metodo PrivateKey. Delete</span><span class="sxs-lookup"><span data-stu-id="6b422-103">PrivateKey.Delete method</span></span>

<span data-ttu-id="6b422-104">\[Il metodo **Delete** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="6b422-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6b422-105">Usare invece la [**Proprietà X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6b422-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6b422-106">Il metodo **Delete** Elimina il contenitore di chiavi private a cui fa riferimento l'oggetto [**PrivateKey**](privatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="6b422-106">The **Delete** method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b422-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b422-107">Syntax</span></span>


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a><span data-ttu-id="6b422-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b422-108">Parameters</span></span>

<span data-ttu-id="6b422-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6b422-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b422-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b422-110">Return value</span></span>

<span data-ttu-id="6b422-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6b422-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b422-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b422-112">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b422-113">Questo metodo elimina il contenitore di chiavi private a cui fa riferimento l'oggetto [**PrivateKey**](privatekey.md) , nonché tutte le chiavi private nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="6b422-113">This method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object as well as all private keys in the container.</span></span> <span data-ttu-id="6b422-114">Qualsiasi elemento crittografato con le chiavi pubbliche corrispondenti alle chiavi private eliminate non sarà più possibile decrittografare.</span><span class="sxs-lookup"><span data-stu-id="6b422-114">Anything encrypted using the public keys corresponding to the deleted private keys will no longer be able to be decrypted.</span></span>

 

<span data-ttu-id="6b422-115">Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="6b422-115">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b422-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b422-116">Requirements</span></span>



| <span data-ttu-id="6b422-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b422-117">Requirement</span></span> | <span data-ttu-id="6b422-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6b422-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b422-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6b422-119">Redistributable</span></span><br/> | <span data-ttu-id="6b422-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b422-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6b422-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6b422-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="6b422-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b422-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
