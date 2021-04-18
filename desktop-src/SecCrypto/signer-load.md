---
description: Carica un certificato di firma da un file con estensione pfx specificato.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Metodo signer. Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330270"
---
# <a name="signerload-method"></a><span data-ttu-id="e0376-103">Metodo signer. Load</span><span class="sxs-lookup"><span data-stu-id="e0376-103">Signer.Load method</span></span>

<span data-ttu-id="e0376-104">\[Il metodo **Load** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e0376-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e0376-105">Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e0376-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e0376-106">Il metodo **Load** carica un certificato di firma da un file con estensione pfx specificato.</span><span class="sxs-lookup"><span data-stu-id="e0376-106">The **Load** method loads a signing certificate from a specified .pfx file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0376-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0376-107">Syntax</span></span>


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e0376-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0376-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0376-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="e0376-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="e0376-110">Nome del file con estensione PFX contenente il certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="e0376-110">Name of the .pfx file that contains the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="e0376-111">*Password* \[ di opzionale\]</span><span class="sxs-lookup"><span data-stu-id="e0376-111">*Password* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0376-112">Stringa contenente la password in testo non crittografato utilizzata per aprire il file.</span><span class="sxs-lookup"><span data-stu-id="e0376-112">String containing the plaintext password used to open the file.</span></span> <span data-ttu-id="e0376-113">Per la password è possibile usare fino a 32 caratteri Unicode, incluso un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e0376-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="e0376-114">Il valore predefinito è una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="e0376-114">The default value is an empty string ("").</span></span> <span data-ttu-id="e0376-115">Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="e0376-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0376-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0376-116">Return value</span></span>

<span data-ttu-id="e0376-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e0376-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0376-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0376-118">Remarks</span></span>

<span data-ttu-id="e0376-119">Questo metodo carica il primo certificato nel file con estensione pfx a cui è associata una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="e0376-119">This method loads the first certificate in the .pfx file that has a private key associated with it.</span></span>

<span data-ttu-id="e0376-120">Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="e0376-120">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0376-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0376-121">Requirements</span></span>



| <span data-ttu-id="e0376-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0376-122">Requirement</span></span> | <span data-ttu-id="e0376-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e0376-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0376-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e0376-124">Redistributable</span></span><br/> | <span data-ttu-id="e0376-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0376-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e0376-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e0376-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="e0376-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0376-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0376-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0376-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0376-129">**Firmatario**</span><span class="sxs-lookup"><span data-stu-id="e0376-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
