---
title: MDM_EnterpriseModernAppManagement_StoreLicenses02_01 classe
description: La classe MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 01 viene usata per gestire \_ le licenze per le app dello Store.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 classe
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 classe, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0342acc9cb74825552a409d686e5bc55f0cebc75642d5981a7144f3bac74bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018109"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a>Classe \_ MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** viene usata per gestire le licenze per le app dello Store.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a>Members

La **classe MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** include questi metodi.



| Metodo                                                                                                              | Descrizione                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [**AddLicenseMethod**](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | Metodo per l'aggiunta di una licenza.<br/>                 |
| [**GetLicenseFromStoreMethod**](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | Metodo per ottenere una licenza dallo store.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** ha queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo facoltativo. ID licenza per un'app dello Store installata. L'ID licenza è in genere il nome PFN dell'app.

Le operazioni supportate sono Add, Get ed Delete.

</dd> <dt>

[LicenseCategory](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[LicenseUsage](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"

</dd> <dt>

[RequesterID](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

