---
description: Recupera un valore booleano che indica se il certificato è per un'autorità di certificazione (CA).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: Proprietà BasicConstraints. IsCertificateAuthority
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331308"
---
# <a name="basicconstraintsiscertificateauthority-property"></a><span data-ttu-id="aee37-103">Proprietà BasicConstraints. IsCertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="aee37-103">BasicConstraints.IsCertificateAuthority property</span></span>

<span data-ttu-id="aee37-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aee37-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="aee37-105">Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="aee37-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="aee37-106">La proprietà **IsCertificateAuthority** recupera un valore booleano che indica se il certificato è per un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="aee37-106">The **IsCertificateAuthority** property retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="aee37-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="aee37-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee37-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aee37-108">Syntax</span></span>


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a><span data-ttu-id="aee37-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aee37-109">Property value</span></span>

<span data-ttu-id="aee37-110">Se **true**, il certificato deve essere usato solo da un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="aee37-110">If **True**, the certificate is to be used only by a CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee37-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aee37-111">Requirements</span></span>



| <span data-ttu-id="aee37-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee37-112">Requirement</span></span> | <span data-ttu-id="aee37-113">Valore</span><span class="sxs-lookup"><span data-stu-id="aee37-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee37-114">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="aee37-114">End of client support</span></span><br/> | <span data-ttu-id="aee37-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee37-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aee37-116">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="aee37-116">End of server support</span></span><br/> | <span data-ttu-id="aee37-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aee37-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aee37-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="aee37-118">Redistributable</span></span><br/>       | <span data-ttu-id="aee37-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="aee37-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aee37-120">DLL</span><span class="sxs-lookup"><span data-stu-id="aee37-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="aee37-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee37-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
