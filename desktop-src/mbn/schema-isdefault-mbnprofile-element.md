---
description: Specifica se questo è il profilo predefinito per il dispositivo.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Elemento IsDefault (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484828"
---
# <a name="isdefault-mbnprofile-element"></a><span data-ttu-id="139cb-103">Elemento IsDefault (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="139cb-103">IsDefault (MBNProfile) Element</span></span>

<span data-ttu-id="139cb-104">L'elemento **IsDefault (MBNProfile)** specifica se questo è il profilo predefinito per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="139cb-104">The **IsDefault (MBNProfile)** element specifies if this is the default profile for the device.</span></span>

<span data-ttu-id="139cb-105">Si tratta di un elemento facoltativo e, se non è specificato, il profilo non verrà impostato come profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="139cb-105">This is an optional element and if it is not specified then the profile will not be set as the default profile.</span></span>

<span data-ttu-id="139cb-106">Il profilo predefinito viene usato dal servizio Mobile Broadband per gli scopi seguenti</span><span class="sxs-lookup"><span data-stu-id="139cb-106">The default profile is used by the Mobile Broadband service for following purposes</span></span>

-   <span data-ttu-id="139cb-107">Il servizio Mobile Broadband usa le impostazioni di connessione del profilo predefinito durante l'esecuzione di connessioni di rete automatiche.</span><span class="sxs-lookup"><span data-stu-id="139cb-107">The Mobile Broadband service uses connection settings from the default profile when performing automatic network connections.</span></span> <span data-ttu-id="139cb-108">Queste impostazioni includono il nome del punto di accesso, il nome utente, la password e così via.</span><span class="sxs-lookup"><span data-stu-id="139cb-108">These settings include access point name, user name, password, etc.</span></span>
-   <span data-ttu-id="139cb-109">Il criterio di connessione automatica per un dispositivo mobile broadband viene tratto dal profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="139cb-109">Auto connection policy for a Mobile Broadband device is taken from it's default profile.</span></span>
-   <span data-ttu-id="139cb-110">L'interfaccia utente della connessione di rete del sistema operativo usa anche i dati di connessione del profilo predefinito per le operazioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="139cb-110">The operating system network connection UI also uses connection data from the default profile for connection operations.</span></span>

<span data-ttu-id="139cb-111">I provider di servizi cellulari possono fornire i dettagli della connessione in un profilo e configurare tale profilo come profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="139cb-111">Cellular service providers can provide the connection details in a profile and configure that profile as a default profile.</span></span> <span data-ttu-id="139cb-112">Il servizio Mobile Broadband utilizzerà queste impostazioni di connessione senza richiedere informazioni all'utente.</span><span class="sxs-lookup"><span data-stu-id="139cb-112">The Mobile Broadband service will use these connection settings without prompting user for details.</span></span>

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

<span data-ttu-id="139cb-113">L'elemento **IsDefault** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="139cb-113">The **IsDefault** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="139cb-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="139cb-114">Requirements</span></span>



| <span data-ttu-id="139cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="139cb-115">Requirement</span></span> | <span data-ttu-id="139cb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="139cb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="139cb-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="139cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="139cb-118">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="139cb-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="139cb-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="139cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="139cb-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="139cb-120">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="139cb-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="139cb-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="139cb-122">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="139cb-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="139cb-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="139cb-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="139cb-124">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="139cb-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="139cb-125">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="139cb-125">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




