---
description: Aggiunge un oggetto certificato a un archivio certificati aperto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330267"
---
# <a name="storeadd-method"></a><span data-ttu-id="fe25a-103">Store. Add (metodo)</span><span class="sxs-lookup"><span data-stu-id="fe25a-103">Store.Add method</span></span>

<span data-ttu-id="fe25a-104">\[Il metodo **Add** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fe25a-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fe25a-105">Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fe25a-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fe25a-106">Il metodo **Add** aggiunge un oggetto [**certificato**](certificate.md) a un [*archivio certificati*](../secgloss/c-gly.md)aperto.</span><span class="sxs-lookup"><span data-stu-id="fe25a-106">The **Add** method adds a [**Certificate**](certificate.md) object to an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="fe25a-107">Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fe25a-107">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe25a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe25a-108">Syntax</span></span>


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="fe25a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe25a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe25a-110">*Certificato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fe25a-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe25a-111">Espressione che viene risolta in un oggetto [**certificato**](certificate.md) da aggiungere all'archivio.</span><span class="sxs-lookup"><span data-stu-id="fe25a-111">Expression that resolves to a [**Certificate**](certificate.md) object to be added to the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe25a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe25a-112">Return value</span></span>

<span data-ttu-id="fe25a-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fe25a-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe25a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe25a-114">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe25a-115">Quando questo metodo viene chiamato in un archivio di sistema da uno script Web, lo script deve accedere ai certificati digitali nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="fe25a-115">When this method is called on a system store from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="fe25a-116">Se si consente allo script di accedere ai certificati digitali, il sito Web da cui viene eseguito lo script otterrà anche l'accesso a tutte le informazioni personali archiviate nei certificati.</span><span class="sxs-lookup"><span data-stu-id="fe25a-116">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="fe25a-117">La prima volta che questo metodo viene chiamato da un particolare dominio, viene generata una finestra di dialogo in cui l'utente deve indicare se l'accesso ai certificati deve essere consentito.</span><span class="sxs-lookup"><span data-stu-id="fe25a-117">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="fe25a-118">Se l'archivio non è aperto in modalità di lettura/scrittura, questo metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="fe25a-118">If the store is not open in read/write mode, this method fails.</span></span> <span data-ttu-id="fe25a-119">Sebbene questo metodo possa essere utilizzato con gli archivi di memoria, le modifiche apportate a un archivio di memoria non vengono rese permanente quando l'archivio viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="fe25a-119">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

<span data-ttu-id="fe25a-120">Se il certificato da aggiungere all'archivio è identico a quello già presente, il metodo **Add** Elimina il certificato esistente dall'archivio e quindi aggiunge il nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="fe25a-120">If the certificate being added to the store is the same as one that is already there, the **Add** method deletes the existing certificate from the store and then adds the new certificate.</span></span> <span data-ttu-id="fe25a-121">Il nuovo certificato eredita le proprietà dal certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="fe25a-121">The new certificate inherits properties from the existing certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe25a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe25a-122">Requirements</span></span>



| <span data-ttu-id="fe25a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe25a-123">Requirement</span></span> | <span data-ttu-id="fe25a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fe25a-124">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe25a-125">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fe25a-125">Redistributable</span></span><br/> | <span data-ttu-id="fe25a-126">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe25a-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fe25a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fe25a-127">DLL</span></span><br/>             | <dl> <span data-ttu-id="fe25a-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe25a-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe25a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe25a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe25a-130">**Store**</span><span class="sxs-lookup"><span data-stu-id="fe25a-130">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="fe25a-131">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="fe25a-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
