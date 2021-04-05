---
title: Tipo complesso CredentialsSourceParameters
description: Definisce l'elemento necessario per specificare l'origine del certificato da utilizzare con un'autenticazione EAP-TLS.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- CredentialsSourceParameters di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120563"
---
# <a name="credentialssourceparameters-complex-type"></a><span data-ttu-id="37bb2-104">Tipo complesso CredentialsSourceParameters</span><span class="sxs-lookup"><span data-stu-id="37bb2-104">CredentialsSourceParameters Complex Type</span></span>

<span data-ttu-id="37bb2-105">Il tipo complesso **CredentialsSourceParameters** definisce l'elemento necessario per specificare l'origine del certificato da usare con un'autenticazione EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="37bb2-105">The **CredentialsSourceParameters** complex type defines the element required to specify the source of the certificate to be used with an EAP-TLS authentication.</span></span>

<span data-ttu-id="37bb2-106">Esiste una scelta tra l'elemento [**smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) o l'elemento [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="37bb2-106">There is a choice between the [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) element or [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) element.</span></span>

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="37bb2-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="37bb2-107">Child elements</span></span>



| <span data-ttu-id="37bb2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="37bb2-108">Element</span></span>                                                                                                             | <span data-ttu-id="37bb2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="37bb2-109">Type</span></span>                                                                                  | <span data-ttu-id="37bb2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37bb2-110">Description</span></span>                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37bb2-111">**CertificateStore**</span><span class="sxs-lookup"><span data-stu-id="37bb2-111">**CertificateStore**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [<span data-ttu-id="37bb2-112">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="37bb2-112">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | <span data-ttu-id="37bb2-113">Indica che EAP-TLS deve leggere il certificato dall'archivio personale dell'utente o dal computer in fase di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="37bb2-113">Indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span> <br/> |
| [<span data-ttu-id="37bb2-114">**Smart Card**</span><span class="sxs-lookup"><span data-stu-id="37bb2-114">**SmartCard**</span></span>](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [<span data-ttu-id="37bb2-115">**emptyString**</span><span class="sxs-lookup"><span data-stu-id="37bb2-115">**emptyString**</span></span>](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | <span data-ttu-id="37bb2-116">Indica che EAP-TLS deve leggere il certificato dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="37bb2-116">Indicates that EAP-TLS should read the certificate from the Smart Card.</span></span> <br/>                                          |



## <a name="remarks"></a><span data-ttu-id="37bb2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="37bb2-117">Remarks</span></span>

<span data-ttu-id="37bb2-118">Gli elementi [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) e [**smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) non possono essere usati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="37bb2-118">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="37bb2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37bb2-119">Requirements</span></span>



| <span data-ttu-id="37bb2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="37bb2-120">Requirement</span></span> | <span data-ttu-id="37bb2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="37bb2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37bb2-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37bb2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="37bb2-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37bb2-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="37bb2-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37bb2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="37bb2-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="37bb2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37bb2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37bb2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37bb2-127">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="37bb2-127">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="37bb2-128">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="37bb2-128">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="37bb2-129">Tipi complessi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="37bb2-129">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





