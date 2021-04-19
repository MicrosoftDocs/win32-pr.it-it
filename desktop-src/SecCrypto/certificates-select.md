---
description: Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'Metodo ICertificates2:: Select'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333162"
---
# <a name="icertificates2select-method"></a><span data-ttu-id="732d2-103">Metodo ICertificates2:: Select</span><span class="sxs-lookup"><span data-stu-id="732d2-103">ICertificates2::Select method</span></span>

<span data-ttu-id="732d2-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="732d2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="732d2-105">Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="732d2-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="732d2-106">Il metodo **Select** Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati.</span><span class="sxs-lookup"><span data-stu-id="732d2-106">The **Select** method displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span> <span data-ttu-id="732d2-107">Questo metodo è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="732d2-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="732d2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="732d2-108">Syntax</span></span>


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a><span data-ttu-id="732d2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="732d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="732d2-110">*Titolo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="732d2-110">*Title* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="732d2-111">Stringa che contiene il titolo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="732d2-111">String that contains the title for the dialog box.</span></span> <span data-ttu-id="732d2-112">Il valore predefinito è una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="732d2-112">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="732d2-113">*DisplayString* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="732d2-113">*DisplayString* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="732d2-114">Stringa che contiene il testo della richiesta visualizzato con la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="732d2-114">String that contains the prompt text displayed with the dialog box.</span></span> <span data-ttu-id="732d2-115">Il valore predefinito è una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="732d2-115">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="732d2-116">*bMultiSelect* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="732d2-116">*bMultiSelect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="732d2-117">Valore booleano che indica se l'utente può selezionare più di un certificato.</span><span class="sxs-lookup"><span data-stu-id="732d2-117">Boolean value that indicates whether the user can select more than one certificate.</span></span> <span data-ttu-id="732d2-118">True indica che è possibile selezionare più certificati utilizzando il tasto CTRL o MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="732d2-118">True indicates multiple certificates can be selected by using the CTRL or SHIFT key.</span></span> <span data-ttu-id="732d2-119">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="732d2-119">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="732d2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="732d2-120">Return value</span></span>

<span data-ttu-id="732d2-121">Oggetto [**Certificates**](certificates.md) che contiene i certificati selezionati dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="732d2-121">A [**Certificates**](certificates.md) object that contains the certificates selected from the dialog box.</span></span>

<span data-ttu-id="732d2-122">**Capicom 2,1:** L'oggetto [**certificati**](certificates.md) restituito contiene riferimenti ai certificati della raccolta da cui è stata effettuata la selezione.</span><span class="sxs-lookup"><span data-stu-id="732d2-122">**CAPICOM 2.1:** The [**Certificates**](certificates.md) object that is returned contains references to the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="732d2-123">Tutte le modifiche apportate ai certificati nell'oggetto **certificati** restituiti vengono riflesse in tale raccolta.</span><span class="sxs-lookup"><span data-stu-id="732d2-123">Any changes made to the certificates in the returned **Certificates** object are reflected in that collection.</span></span>

<span data-ttu-id="732d2-124">**CApicol 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 e CApicol 2.0.0.3:** L'oggetto [**certificati**](certificates.md) restituito contiene copie dei certificati della raccolta da cui è stata effettuata la selezione.</span><span class="sxs-lookup"><span data-stu-id="732d2-124">**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2, and CAPICOM 2.0.0.3:** The [**Certificates**](certificates.md) object that is returned contains copies of the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="732d2-125">Tutte le modifiche apportate ai certificati nell'oggetto **certificati** restituiti non vengono riflesse in tale raccolta.</span><span class="sxs-lookup"><span data-stu-id="732d2-125">Any changes made to the certificates in the returned **Certificates** object are not reflected in that collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="732d2-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="732d2-126">Requirements</span></span>



| <span data-ttu-id="732d2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="732d2-127">Requirement</span></span> | <span data-ttu-id="732d2-128">Valore</span><span class="sxs-lookup"><span data-stu-id="732d2-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="732d2-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="732d2-129">End of client support</span></span><br/> | <span data-ttu-id="732d2-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="732d2-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="732d2-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="732d2-131">End of server support</span></span><br/> | <span data-ttu-id="732d2-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="732d2-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="732d2-133">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="732d2-133">Redistributable</span></span><br/>       | <span data-ttu-id="732d2-134">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="732d2-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="732d2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="732d2-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="732d2-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="732d2-136"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
