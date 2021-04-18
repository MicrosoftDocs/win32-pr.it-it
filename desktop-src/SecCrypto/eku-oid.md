---
description: Imposta o Recupera una stringa che contiene un valore stringa dell'OID EKU come definito in WinCrypt. h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'Proprietà IEKU:: OID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330272"
---
# <a name="iekuoid-property"></a><span data-ttu-id="40a93-103">Proprietà IEKU:: OID</span><span class="sxs-lookup"><span data-stu-id="40a93-103">IEKU::OID property</span></span>

<span data-ttu-id="40a93-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="40a93-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="40a93-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="40a93-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="40a93-106">La proprietà **OID** imposta o Recupera una stringa che contiene un valore stringa dell'OID EKU come definito in WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="40a93-106">The **OID** property sets or retrieves a string that contains an EKU OID string value as defined in Wincrypt.h.</span></span>

<span data-ttu-id="40a93-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="40a93-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a93-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40a93-108">Syntax</span></span>


```VB
EKU.OID As String
```



## <a name="property-value"></a><span data-ttu-id="40a93-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="40a93-109">Property value</span></span>

<span data-ttu-id="40a93-110">Stringa che contiene il valore stringa dell'OID EKU come definito in WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="40a93-110">String that contains the EKU OID string value as defined in Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="40a93-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="40a93-111">Remarks</span></span>

<span data-ttu-id="40a93-112">Questa proprietà non usa l'oggetto [**OID**](oid.md) introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="40a93-112">This property does not use the [**OID**](oid.md) object introduced in CAPICOM 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a93-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40a93-113">Requirements</span></span>



| <span data-ttu-id="40a93-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a93-114">Requirement</span></span> | <span data-ttu-id="40a93-115">Valore</span><span class="sxs-lookup"><span data-stu-id="40a93-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40a93-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="40a93-116">End of client support</span></span><br/> | <span data-ttu-id="40a93-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40a93-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="40a93-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="40a93-118">End of server support</span></span><br/> | <span data-ttu-id="40a93-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40a93-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="40a93-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="40a93-120">Redistributable</span></span><br/>       | <span data-ttu-id="40a93-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="40a93-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="40a93-122">DLL</span><span class="sxs-lookup"><span data-stu-id="40a93-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="40a93-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40a93-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
