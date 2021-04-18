---
title: Elemento EapType (mschapv2connectionpropertiesv1schema)
description: È un tipo derivato dell'elemento EapType dello schema baseeapconnectionpropertiesv1. Si tratta dell'elemento principale che viene visualizzato all'interno dell'elemento config dello schema EapHostConfig.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334318"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a><span data-ttu-id="b2e67-105">Elemento EapType (mschapv2connectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="b2e67-105">EapType Element (mschapv2connectionpropertiesv1schema)</span></span>

<span data-ttu-id="b2e67-106">L'elemento **EapType** è un tipo derivato dell'elemento [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) dello schema [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="b2e67-106">The **EapType** element is a derived type of the [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span> <span data-ttu-id="b2e67-107">Si tratta dell'elemento principale visualizzato all'interno dell'elemento config dello schema [EapHostConfig](eaphostconfigschema-elements.md)</span><span class="sxs-lookup"><span data-stu-id="b2e67-107">This is the top element that appears inside the Config element of the [EapHostConfig](eaphostconfigschema-elements.md) schema</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="b2e67-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b2e67-108">Child elements</span></span>



| <span data-ttu-id="b2e67-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b2e67-109">Element</span></span>                                                                                                       | <span data-ttu-id="b2e67-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2e67-110">Type</span></span>    | <span data-ttu-id="b2e67-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2e67-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2e67-112">**UseWinLogonCredentials**</span><span class="sxs-lookup"><span data-stu-id="b2e67-112">**UseWinLogonCredentials**</span></span>](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | <span data-ttu-id="b2e67-113">boolean</span><span class="sxs-lookup"><span data-stu-id="b2e67-113">boolean</span></span> | <span data-ttu-id="b2e67-114">Controlla l'uso delle credenziali WinLogin.</span><span class="sxs-lookup"><span data-stu-id="b2e67-114">Controls use of the winlogin credentials.</span></span> <span data-ttu-id="b2e67-115">Se TRUE, EAP MS-CHAPv2 ottiene le credenziali da Winlogon.</span><span class="sxs-lookup"><span data-stu-id="b2e67-115">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="b2e67-116">Se FALSE, EAP MS-CHAPv2 ottiene le credenziali dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b2e67-116">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <br/> <span data-ttu-id="b2e67-117">L'elemento [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b2e67-117">The [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b2e67-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2e67-118">Remarks</span></span>

<span data-ttu-id="b2e67-119">L'elemento **processContents** consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="b2e67-119">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="b2e67-120">L'elemento **processContents** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b2e67-120">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e67-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2e67-121">Requirements</span></span>



| <span data-ttu-id="b2e67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e67-122">Requirement</span></span> | <span data-ttu-id="b2e67-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b2e67-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2e67-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2e67-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e67-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2e67-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2e67-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2e67-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e67-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2e67-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2e67-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2e67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e67-129">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="b2e67-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b2e67-130">Schema mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b2e67-130">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





