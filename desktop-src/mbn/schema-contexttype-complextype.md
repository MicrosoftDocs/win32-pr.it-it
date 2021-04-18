---
description: Specifica il contesto connenction di un dispositivo mobile broadband.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: Tipo complesso contextType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306780"
---
# <a name="contexttype-complex-type"></a><span data-ttu-id="20ea1-103">Tipo complesso contextType</span><span class="sxs-lookup"><span data-stu-id="20ea1-103">contextType Complex Type</span></span>

<span data-ttu-id="20ea1-104">Il tipo complesso **contextType** specifica il contesto connenction di un dispositivo mobile broadband.</span><span class="sxs-lookup"><span data-stu-id="20ea1-104">The **contextType** complex type specifies the connenction context of a Mobile Broadband device.</span></span>

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="UserName"
                        type="nameType"
                     />
                    <xs:element name="IgnorePassword"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="20ea1-105">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="20ea1-105">Child elements</span></span>



| <span data-ttu-id="20ea1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="20ea1-106">Element</span></span>                                                               | <span data-ttu-id="20ea1-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="20ea1-107">Type</span></span>                                           | <span data-ttu-id="20ea1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ea1-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20ea1-109">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="20ea1-109">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)       |                                                | <span data-ttu-id="20ea1-110">APN o stringa di connessione da usare per stabilire una connessione dati</span><span class="sxs-lookup"><span data-stu-id="20ea1-110">APN or dial string to be used to establish a data connection</span></span><br/>                        |
| [<span data-ttu-id="20ea1-111">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="20ea1-111">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)       |                                                | <span data-ttu-id="20ea1-112">Protocollo di autenticazione da usare per l'attivazione di un contesto di PDP.</span><span class="sxs-lookup"><span data-stu-id="20ea1-112">Authentication protocol to be used for activating a PDP context.</span></span><br/>                    |
| [<span data-ttu-id="20ea1-113">**Compressione**</span><span class="sxs-lookup"><span data-stu-id="20ea1-113">**Compression**</span></span>](schema-compression-contexttype-element.md)         |                                                | <span data-ttu-id="20ea1-114">Specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati</span><span class="sxs-lookup"><span data-stu-id="20ea1-114">Specifies if compression will be used at the data link for header and data transfer</span></span><br/> |
| [<span data-ttu-id="20ea1-115">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="20ea1-115">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="20ea1-116">boolean</span><span class="sxs-lookup"><span data-stu-id="20ea1-116">boolean</span></span>                                        | <span data-ttu-id="20ea1-117">Come gestire le password durante l'aggiornamento dei profili.</span><span class="sxs-lookup"><span data-stu-id="20ea1-117">How to handle passwords when upgrading profiles.</span></span><br/>                                    |
| [<span data-ttu-id="20ea1-118">**Password**</span><span class="sxs-lookup"><span data-stu-id="20ea1-118">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="20ea1-119">string</span><span class="sxs-lookup"><span data-stu-id="20ea1-119">string</span></span>                                         | <span data-ttu-id="20ea1-120">Password utilizzata per autenticare un utente</span><span class="sxs-lookup"><span data-stu-id="20ea1-120">Password used to authenticate a user</span></span><br/>                                                |
| [<span data-ttu-id="20ea1-121">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="20ea1-121">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)     |                                                | <span data-ttu-id="20ea1-122">Accedere alle credenziali per una connessione.</span><span class="sxs-lookup"><span data-stu-id="20ea1-122">Log on credentials for a connection.</span></span><br/>                                                |
| [<span data-ttu-id="20ea1-123">**Nome utente**</span><span class="sxs-lookup"><span data-stu-id="20ea1-123">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="20ea1-124">**nameType**</span><span class="sxs-lookup"><span data-stu-id="20ea1-124">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="20ea1-125">Nome utente per l'accesso</span><span class="sxs-lookup"><span data-stu-id="20ea1-125">User name for logon</span></span><br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="20ea1-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20ea1-126">Requirements</span></span>



| <span data-ttu-id="20ea1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="20ea1-127">Requirement</span></span> | <span data-ttu-id="20ea1-128">Valore</span><span class="sxs-lookup"><span data-stu-id="20ea1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="20ea1-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20ea1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="20ea1-130">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="20ea1-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="20ea1-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20ea1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="20ea1-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="20ea1-132">None supported</span></span><br/>                         |



 

 




