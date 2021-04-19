---
description: Il metodo Remove rimuove un certificato da un archivio certificati aperto. Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327083"
---
# <a name="storeremove-method"></a><span data-ttu-id="848cd-104">Store. Remove (metodo)</span><span class="sxs-lookup"><span data-stu-id="848cd-104">Store.Remove method</span></span>

<span data-ttu-id="848cd-105">\[Il metodo **Remove** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="848cd-105">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="848cd-106">Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="848cd-106">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="848cd-107">Il metodo **Remove** rimuove un [*certificato*](../secgloss/c-gly.md) da un [*archivio certificati*](../secgloss/c-gly.md)aperto.</span><span class="sxs-lookup"><span data-stu-id="848cd-107">The **Remove** method removes a [*certificate*](../secgloss/c-gly.md) from an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="848cd-108">Questo metodo può essere utilizzato solo con un archivio che è stato aperto con l'autorizzazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="848cd-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="848cd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="848cd-109">Syntax</span></span>


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="848cd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="848cd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="848cd-111">*Certificato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="848cd-111">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="848cd-112">Espressione che viene risolta in un'istanza di un oggetto [**certificato**](certificate.md) da rimuovere dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="848cd-112">Expression that resolves to an instance of a [**Certificate**](certificate.md) object to be removed from the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="848cd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="848cd-113">Return value</span></span>

<span data-ttu-id="848cd-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="848cd-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="848cd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="848cd-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="848cd-116">Quando questo metodo viene chiamato da uno script Web, lo script deve eliminare i certificati digitali dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="848cd-116">When this method is called from a web script, the script needs to delete digital certificates from the local computer.</span></span> <span data-ttu-id="848cd-117">Consentire ai siti Web non attendibili di eliminare i certificati digitali costituisce un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="848cd-117">Allowing untrusted websites to delete digital certificates is a security risk.</span></span> <span data-ttu-id="848cd-118">Viene visualizzata una finestra di dialogo in cui viene chiesto se il sito Web può eliminare i certificati quando questo metodo viene chiamato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="848cd-118">A dialog box that asks whether the website can delete certificates appears when this method is first called.</span></span> <span data-ttu-id="848cd-119">Se si consente all'applicazione di eliminare i certificati e selezionare "non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per gli script che eliminano i certificati all'interno di tale dominio.</span><span class="sxs-lookup"><span data-stu-id="848cd-119">If you allow the application to delete certificates and select "Do not show this dialog box again," the dialog box will no longer appear for any script that deletes certificates within that domain.</span></span> <span data-ttu-id="848cd-120">Tuttavia, gli script esterni al dominio che tentano di eliminare i certificati continueranno a causare la visualizzazione di questa finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="848cd-120">However, scripts outside that domain that attempt to delete certificates will still cause this dialog box to appear.</span></span> <span data-ttu-id="848cd-121">Se non si consente allo script di eliminare i certificati e selezionare "non visualizzare più questa finestra di dialogo", gli script all'interno di tale dominio verranno automaticamente rifiutati la possibilità di eliminare i certificati.</span><span class="sxs-lookup"><span data-stu-id="848cd-121">If you do not allow the script to delete certificates and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to delete certificates.</span></span>

 

<span data-ttu-id="848cd-122">Quando si elimina un certificato da un archivio, è necessario innanzitutto eliminare la chiave privata associata al certificato.</span><span class="sxs-lookup"><span data-stu-id="848cd-122">When you delete a certificate from a store, you should first delete the private key associated with the certificate.</span></span>

<span data-ttu-id="848cd-123">Se l'archivio non è aperto con l'autorizzazione di lettura/scrittura, questo metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="848cd-123">If the store is not open with read/write permission, this method fails.</span></span> <span data-ttu-id="848cd-124">Sebbene questo metodo possa essere utilizzato con gli archivi di memoria, le modifiche apportate a un archivio di memoria non vengono rese permanente quando l'archivio viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="848cd-124">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="848cd-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="848cd-125">Requirements</span></span>



| <span data-ttu-id="848cd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="848cd-126">Requirement</span></span> | <span data-ttu-id="848cd-127">Valore</span><span class="sxs-lookup"><span data-stu-id="848cd-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="848cd-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="848cd-128">Redistributable</span></span><br/> | <span data-ttu-id="848cd-129">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="848cd-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="848cd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="848cd-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="848cd-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="848cd-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="848cd-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="848cd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="848cd-133">**Store**</span><span class="sxs-lookup"><span data-stu-id="848cd-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="848cd-134">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="848cd-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
