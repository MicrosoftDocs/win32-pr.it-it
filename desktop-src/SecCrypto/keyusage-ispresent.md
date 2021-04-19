---
description: Recupera un valore booleano che indica se l'estensione per l'utilizzo di dati è presente.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: Proprietà DataUsage. Presenter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323945"
---
# <a name="keyusageispresent-property"></a><span data-ttu-id="68b0a-103">Proprietà DataUsage. Presenter</span><span class="sxs-lookup"><span data-stu-id="68b0a-103">KeyUsage.IsPresent property</span></span>

<span data-ttu-id="68b0a-104">\[La proprietà **impresent** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="68b0a-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="68b0a-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="68b0a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="68b0a-106">La proprietà **represent** recupera un valore booleano che indica se l'estensione per l' [**utilizzo di dati**](keyusage.md) è presente.</span><span class="sxs-lookup"><span data-stu-id="68b0a-106">The **IsPresent** property retrieves a Boolean value that indicates whether the [**KeyUsage**](keyusage.md) extension is present.</span></span>

<span data-ttu-id="68b0a-107">Questa proprietà è la proprietà predefinita dell'oggetto [**DataUsage**](keyusage.md) .</span><span class="sxs-lookup"><span data-stu-id="68b0a-107">This property is the default property of the [**KeyUsage**](keyusage.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b0a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68b0a-108">Syntax</span></span>


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="68b0a-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="68b0a-109">Property value</span></span>

<span data-ttu-id="68b0a-110">Se **true**, è presente l'estensione per l'utilizzo di dati.</span><span class="sxs-lookup"><span data-stu-id="68b0a-110">If **true**, the KeyUsage extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b0a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68b0a-111">Requirements</span></span>



| <span data-ttu-id="68b0a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b0a-112">Requirement</span></span> | <span data-ttu-id="68b0a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="68b0a-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b0a-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="68b0a-114">Redistributable</span></span><br/> | <span data-ttu-id="68b0a-115">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="68b0a-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="68b0a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="68b0a-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="68b0a-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68b0a-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b0a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68b0a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b0a-119">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="68b0a-119">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
