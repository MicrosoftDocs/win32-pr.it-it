---
description: Recupera un valore booleano che indica se l'estensione di vincolo di base è contrassegnata come critica.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: Proprietà BasicConstraints. Critical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8f3f61a0c458229977abae60258ba4cb71420e72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331307"
---
# <a name="basicconstraintsiscritical-property"></a><span data-ttu-id="a36ec-103">Proprietà BasicConstraints. Critical</span><span class="sxs-lookup"><span data-stu-id="a36ec-103">BasicConstraints.IsCritical property</span></span>

<span data-ttu-id="a36ec-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a36ec-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="a36ec-105">Usare invece la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="a36ec-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="a36ec-106">La proprietà **ipocrita** recupera un valore booleano che indica se l'estensione di vincolo di base è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="a36ec-106">The **IsCritical** property retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span>

<span data-ttu-id="a36ec-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a36ec-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a36ec-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a36ec-108">Syntax</span></span>


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a36ec-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a36ec-109">Property value</span></span>

<span data-ttu-id="a36ec-110">Se **true**, l'estensione del vincolo di base è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="a36ec-110">If **true**, the basic constraint extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="a36ec-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a36ec-111">Requirements</span></span>



| <span data-ttu-id="a36ec-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a36ec-112">Requirement</span></span> | <span data-ttu-id="a36ec-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a36ec-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a36ec-114">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a36ec-114">End of client support</span></span><br/> | <span data-ttu-id="a36ec-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a36ec-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a36ec-116">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a36ec-116">End of server support</span></span><br/> | <span data-ttu-id="a36ec-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a36ec-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a36ec-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a36ec-118">Redistributable</span></span><br/>       | <span data-ttu-id="a36ec-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="a36ec-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a36ec-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a36ec-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a36ec-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a36ec-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
