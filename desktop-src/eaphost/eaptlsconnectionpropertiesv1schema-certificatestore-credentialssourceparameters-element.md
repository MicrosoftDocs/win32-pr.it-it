---
title: Elemento CertificateStore (CredentialsSourceParameters)
description: Indica che EAP-TLS deve leggere il certificato dall'archivio personale dell'utente o dal computer in fase di autenticazione.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Elemento CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518333"
---
# <a name="certificatestore-credentialssourceparameters-element"></a><span data-ttu-id="ee946-104">Elemento CertificateStore (CredentialsSourceParameters)</span><span class="sxs-lookup"><span data-stu-id="ee946-104">CertificateStore (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="ee946-105">L'elemento **CertificateStore (CredentialsSourceParameters)** indica che EAP-TLS deve leggere il certificato dall'archivio personale dell'utente o dal computer in fase di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ee946-105">The **CertificateStore (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span>

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

<span data-ttu-id="ee946-106">L'elemento **CertificateStore** è definito dal tipo complesso [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ee946-106">The **CertificateStore** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee946-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee946-107">Remarks</span></span>

<span data-ttu-id="ee946-108">Gli elementi **CertificateStore** e [**smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) non possono essere usati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="ee946-108">The **CertificateStore** and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee946-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee946-109">Requirements</span></span>



| <span data-ttu-id="ee946-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee946-110">Requirement</span></span> | <span data-ttu-id="ee946-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ee946-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee946-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee946-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ee946-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee946-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee946-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee946-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ee946-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee946-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee946-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee946-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee946-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="ee946-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ee946-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="ee946-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="ee946-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="ee946-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ee946-120">**CredentialsSource (EapType)**</span><span class="sxs-lookup"><span data-stu-id="ee946-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="ee946-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ee946-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ee946-122">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="ee946-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ee946-123">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ee946-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ee946-124">Elementi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ee946-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





