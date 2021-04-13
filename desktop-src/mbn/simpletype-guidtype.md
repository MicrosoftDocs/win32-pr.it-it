---
description: Rappresentazione di stringa di un GUID, nel formato consueto.
MS-HAID: WWAN\_profile\_v4.simpleType\_guidType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: tipo semplice guidType (Mobile Broadband)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b7cc19207ab334694e4b42a49f727070cb385d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526016"
---
# <a name="span-idwwan_profile_v4simpletype_guidtypespanguidtype-simple-type-mobile-broadband"></a><span id="WWAN_profile_v4.simpleType_guidType"></span>tipo semplice guidType (Mobile Broadband)

Rappresentazione di stringa di un GUID, nel formato consueto.

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **guidType** è un token che è limitato dal modello seguente:

-   `{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}}`

 

 



