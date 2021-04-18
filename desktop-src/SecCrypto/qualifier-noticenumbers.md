---
description: Recupera la raccolta di numeri di nota utente.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Proprietà Qualifier. NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329012"
---
# <a name="qualifiernoticenumbers-property"></a><span data-ttu-id="725c4-103">Proprietà Qualifier. NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="725c4-103">Qualifier.NoticeNumbers property</span></span>

<span data-ttu-id="725c4-104">\[La proprietà **NoticeNumbers** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="725c4-104">\[The **NoticeNumbers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="725c4-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="725c4-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="725c4-106">La proprietà **NoticeNumbers** recupera la raccolta di numeri di nota utente.</span><span class="sxs-lookup"><span data-stu-id="725c4-106">The **NoticeNumbers** property retrieves the collection of user notice numbers.</span></span> <span data-ttu-id="725c4-107">Questa proprietà può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="725c4-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="725c4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="725c4-108">Syntax</span></span>


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a><span data-ttu-id="725c4-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="725c4-109">Property value</span></span>

<span data-ttu-id="725c4-110">Raccolta di numeri di nota utente.</span><span class="sxs-lookup"><span data-stu-id="725c4-110">The collection of user notice numbers.</span></span>

## <a name="requirements"></a><span data-ttu-id="725c4-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="725c4-111">Requirements</span></span>



| <span data-ttu-id="725c4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="725c4-112">Requirement</span></span> | <span data-ttu-id="725c4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="725c4-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="725c4-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="725c4-114">Redistributable</span></span><br/> | <span data-ttu-id="725c4-115">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="725c4-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="725c4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="725c4-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="725c4-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="725c4-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725c4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="725c4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725c4-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="725c4-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
