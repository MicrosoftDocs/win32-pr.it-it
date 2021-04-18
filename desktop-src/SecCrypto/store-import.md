---
description: Il metodo di importazione copia in un certificato aperto archivia il contenuto di un archivio certificati precedentemente esportato. Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331264"
---
# <a name="storeimport-method"></a><span data-ttu-id="fb468-104">Store. Import (metodo)</span><span class="sxs-lookup"><span data-stu-id="fb468-104">Store.Import method</span></span>

<span data-ttu-id="fb468-105">\[Il metodo di **importazione** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fb468-105">\[The **Import** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb468-106">Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fb468-106">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fb468-107">Il metodo di **importazione** copia in un [*certificato aperto archivia*](../secgloss/c-gly.md) il contenuto di un archivio certificati precedentemente esportato.</span><span class="sxs-lookup"><span data-stu-id="fb468-107">The **Import** method copies into an open [*certificate store*](../secgloss/c-gly.md) the contents of a previously exported certificate store.</span></span> <span data-ttu-id="fb468-108">Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fb468-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb468-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb468-109">Syntax</span></span>


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a><span data-ttu-id="fb468-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb468-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb468-111">*EncodedStore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb468-111">*EncodedStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb468-112">Stringa che contiene i certificati codificati da importare.</span><span class="sxs-lookup"><span data-stu-id="fb468-112">The string that contains the encoded certificates to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb468-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb468-113">Return value</span></span>

<span data-ttu-id="fb468-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fb468-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb468-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb468-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb468-116">Quando questo metodo viene chiamato da uno script Web, lo script deve accedere ai certificati digitali sul computer locale.</span><span class="sxs-lookup"><span data-stu-id="fb468-116">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="fb468-117">Se si consente allo script di accedere ai certificati digitali, il sito Web da cui viene eseguito lo script otterrà anche l'accesso a tutte le informazioni personali archiviate nei certificati.</span><span class="sxs-lookup"><span data-stu-id="fb468-117">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="fb468-118">La prima volta che questo metodo viene chiamato da un particolare dominio, viene generata una finestra di dialogo in cui l'utente deve indicare se l'accesso ai certificati deve essere consentito.</span><span class="sxs-lookup"><span data-stu-id="fb468-118">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="fb468-119">Se l'archivio non viene aperto con l'autorizzazione di lettura/scrittura, questo metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="fb468-119">If the store is not opened with read/write permission, this method fails.</span></span> <span data-ttu-id="fb468-120">Sebbene questo metodo possa essere utilizzato con gli archivi di memoria, le modifiche apportate a un archivio di memoria non vengono rese permanente quando l'archivio viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="fb468-120">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb468-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb468-121">Requirements</span></span>



| <span data-ttu-id="fb468-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb468-122">Requirement</span></span> | <span data-ttu-id="fb468-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fb468-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb468-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fb468-124">Redistributable</span></span><br/> | <span data-ttu-id="fb468-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb468-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fb468-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fb468-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="fb468-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb468-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb468-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb468-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb468-129">**Store**</span><span class="sxs-lookup"><span data-stu-id="fb468-129">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="fb468-130">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="fb468-130">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
